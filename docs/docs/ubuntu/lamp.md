## Подготовка виртуального сервера LEMP на Ubuntu

### Предварительная подготовка

После создания нового сервера необходимо подключится к нему по ssh

```
ssh root@your_server_ip
```

Затем создадим основного пользователя для ежедневной работы, это нужно чтобы случайно не сломать ничего из под root

```
adduser username
```

На вопросы, которые будет задавать система отвечать можно нажатием Enter, но пароль надо задать сложный Чтобы новый пользователь мог выполнять операции с правами root нужно добавить его в группу sudo

```
usermod -aG sudo username
```

После этого рекомендую добавить ключ к новому пользователю, чтобы в дальнейшем не использовать пароль для входа (команда выполняется на локальном компьютере)

```
ssh-copy-id username@remote_host
```

Предварительно надо сгенерировать ключ на локальном компьютере, для этого использовать утилиту
```
ssh-keygen
```

Для дополнительной безопасности - включить firewall

```
ufw app list
ufw allow OpenSSH
ufw enable
```

Теперь можно подключиться к серверу по ssh под новым пользователем
```
ssh username@remote_host
```

### Установка Nginx

Первым делом установить nginx. При выполнении команды с префиксом sudo система запросит пароль пользователя, необходимо будет ввести пароль для пользователя, который был создан ранее

```
sudo apt update
sudo apt install nginx
```

Если вы не хотите в дальнейшем постоянно вводить пароль при использовании sudo, то можете отредактировать файл ```/etc/sudoers``` поменять строку

```
%sudo   ALL=(ALL:ALL) ALL
```

на
```
%sudo   ALL=(ALL:ALL) NOPASSWD: ALL
```

После установки nginx, команда

```
sudo ufw app list
```

Выведет результат
```
Nginx Full
Nginx HTTP
Nginx HTTPS
OpenSSH
```

Настроим firewall для nginx, на данном этапе разрешаем доступ не шифрованного трафика по порту 80 (ssl еще не настроен)
```
sudo ufw app list
sudo ufw allow 'Nginx HTTP'
```

После этого проверить состояние
```
sudo ufw status
```

Чтобы проверить работоспособность в браузере необходимо перейти по ip адресу вашего сервера, который можно узнать или в панели вашего хостинга или при помощи команды
```
ip addr show eth0 | grep inet | awk '{ print $2; }' | sed 's/\/.*$//'
```

В дальнейшем, если у вас уже есть доменное имя, пропишите А запись в настройках DNS с указанием вашего IP для всех поддоменов (*, www)
Для управления веб сервером используйте следующие команды

```
sudo systemctl stop nginx
sudo systemctl start nginx
sudo systemctl restart nginx
sudo systemctl reload nginx
```

### Настройка хоста

После успешной установки nginx необходимо настроить виртуальный хост для вашего сайта, то, что вы видите в браузере это html страница, которая располагается по адресу /var/www/html/ Добавим дирректорию для нового сайта
```
sudo mkdir -p /var/www/sitename.com/html
```

Так как веб сервер работает обычно от пользователя www-data, то для удобства редактирования файлов добавим текущего пользователя в группу www-data

```
sudo gpasswd -a "$USER" www-data
```

и добавим права на эту дирректорию для текущего пользователя
```
sudo chown -R "$USER":www-data  /var/www/sitename.com/html
```

Файлы конфигурации сервера находятся по адресу ```/etc/nginx/```, где располагаются 2 папки ```sites-available``` и ```sites-enabled``` в первой находятся все конфиги хостов, во второй только активные, обычно файлы из ```sites-available``` переносятся в ```sites-enabled``` при помощи создания ссылки. Создаем новый файл
```
sudo nano /etc/nginx/sites-available/sitename.com
```

вы можете использовать любой другой редактор или перенести файл с локального компьютера при помощи scp Пример содержимого файла
```
server {
        listen *:80;

        root /var/www/sitename.com/html;
        index index.html index.htm;

        server_name sitename.com www.sitename.com;

        location / {
                try_files $uri $uri/ =404;
        }
}
```

теперь активируем хост
```
sudo ln -s /etc/nginx/sites-available/sitename.com /etc/nginx/sites-enabled/
```

Перезапустите nginx
```
udo systemctl restart nginx
```

и откройте/обновите страницу в браузере, теперь вы должны увидеть содержимое файла ```/var/www/sitename.com/html/index.html```

В процессе работы с сервером вам может понадобится менять конфигурацию и проверять работоспособность сервера, список папок и их назначение

- ```/etc/nginx``` - корневая дирректория
- ```/etc/nginx/nginx.conf``` - глобальная конфигурация сервера
- ```/etc/nginx/sites-available/``` - конфигурация всех хостов
- ```/etc/nginx/sites-enabled/``` - ссылки на активные хосты из папки sites-available
- ```/etc/nginx/snippets``` - фрагменты конфигурации
- ```/var/log/nginx/access.log``` - логи доступа, то есть любой запрос к серверу
- ```/var/log/nginx/error.log``` - логи ошибок


### Установка Mysql

```
sudo apt install mysql-server
```

После установки необходимо обновить настройки безопасности
```
sudo mysql_secure_installation
```

Если коротко, то на первый вопрос, про установку плагина VALIDATE PASSWORD PLUGIN отвечаем N, на все остальные Y и задаем сложный пароль для пользователя root, в результате скрипт осуществит определенные манипуляции, которые усилят безопасность сервера, подробные описания этих манипуляций описаны в процессе установки

Чтобы поменять настройки аутентификации с ```auth_socket``` на ```mysql_native_password``` выполните следующие команды
```
sudo mysql // войти в консоль mysql
SELECT user,authentication_string,plugin,host FROM mysql.user; // показать типы аутентификации пользователей
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password'; // обновить метод аутентификации у root и его пароль
FLUSH PRIVILEGES; // применить изменения
exit; // выйти из консоли mysql
```

После внесенный изменений можно проверить, что подключение доступно командой
```
mysql -u root -p
```

Добавить нового пользователя
```
CREATE USER 'newuser'@'localhost' IDENTIFIED BY 'password';
GRANT ALL PRIVILEGES ON dbname . * TO username@localhost; 
FLUSH PRIVILEGES;
```

И создать базу данных
```
CREATE DATABASE `dbname`;
```

### Установка PHP

```
sudo add-apt-repository ppa:ondrej/php
sudo apt update
sudo apt install php7.4 php7.4-common php7.4-cli php7.4-fpm php7.4-gd php7.4-mysql php7.4-mbstring php7.4-curl php7.4-xml php7.4-zip php7.4-json 
```

На этом установка ПО завершена, теперь необходимо скорректировать конфигурацию хоста, созданного ранее, чтобы сервер обрабатывал php скрипты корректно, вернемся к файлу конфигурации хоста и скорректируем его

```
sudo nano /etc/nginx/sites-available/sitename.com
```

В конфигурацию необходимо добавить

```
index index.php index.html index.htm;
```

```
location ~ \.php$ {
    include snippets/fastcgi-php.conf;
    fastcgi_pass unix:/var/run/php/php7.4-fpm.sock;
}
location ~ /\.ht {
    deny all;
}
```

Отключим default хост
```
sudo rm /etc/nginx/sites-enabled/default
```

Проверим, что нет ошибок в файле конфигурации
```
sudo nginx -t
```

Перезагружаем nginx
```
sudo systemctl reload nginx
```

Чтобы проверить, что все настроено верно создайте php скрипт в корневой папке вашего сайта /var/www/sitename.com/html/index.php с любым содержанием, например

```
<?php echo "sitename.com";
```

Обновите страницу в браузере и убедитесь, что там отобразился результат выполнения php скрипта
По умолчанию nginx и php-fpm работают от пользователя www-data, соответственно и все файлы сайта должны принадлежать этому пользователю, чтобы он нормально функционировал, поэтому выполняем команду

```
sudo chown -R www-data:www-data /var/www/sitename.com/html
```

чтобы переназначить владельца файлов и в дальнейшем при каких-либо правках делаем это или от имени www-data или после изменений не забываем менять владельца


## Примеры конфигов

```
worker_processes  4;

error_log  logs/error.log;
pid        logs/nginx.pid;


events {
    worker_connections  1024;
}


http {
    include mime.types;
    client_max_body_size 150m;

    server {
        listen 80;
        server_name gosweb.loc;
        root D:/server/hosts/localsite.loc/public;

        location / {
            try_files $uri /index.php$is_args$args;
        }
 
        location ~ ^/index\.php(/|$) {
            fastcgi_pass 127.0.0.1:9000;
            fastcgi_split_path_info ^(.+\.php)(/.*)$;
            include fastcgi_params;
            fastcgi_param SCRIPT_FILENAME $realpath_root$fastcgi_script_name;
            fastcgi_param DOCUMENT_ROOT $realpath_root;
            internal;
        }
 
        location ~ \.php$ {
            return 404;
        }
 
	    error_log D:/server/hosts/localsite.loc/logs/project_error.log;
	    access_log D:/server/hosts/localsite.loc/logs/project_access.log;
    }

}
```