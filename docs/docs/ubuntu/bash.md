### Автоматический деплой из гита

настроим выполнение команды git pull раз в минуту. Для этого создаём скрипт обновления:
```
nano /var/www/deploy.sh
```
Вставляем в него следующий текст:
```
#!/bin/sh
cd /var/www/site/
git pull > /dev/null
```

Не забываем разрешить выполнение скрипта:
```
chmod +x /var/www/deploy.sh
```

Добавляем скрипт в крон:
```
crontab -e
```

В конец файла копируем строчку:
```
* * * * * /var/www/deploy.sh
```

### пример деплой-файла
```
#!/bin/sh
sudo git pull origin master
sudo composer install
sudo php bin/console doctrine:migrations:migrate -q
sudo php bin/console cache:clear
sudo php bin/console cache:warmup
sudo systemctl restart supervisord
sudo chown -R nginx:nginx ./
```
                               