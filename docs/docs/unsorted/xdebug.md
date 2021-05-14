xdebug

https://stackoverflow.com/questions/41234256/waiting-for-incoming-connection-with-ide-key-phpstorm

sudo apt-get install php7.4-xdebug

video https://www.youtube.com/watch?v=SA_0ZncpSGI

https://www.strangebuzz.com/en/blog/step-by-step-debugging-with-xdebug-symfony-and-phpstorm


установка
sudo apt-get install php-xdebug

включение модуля
sudo phpenmod xdebug


рестарт апача
sudo systemctl restart apache2


/etc/php/7.4/mods-available$ sudo gedit xdebug.ini
sudo subl /etc/php/7.4/mods-available/xdebug.ini

zend_extension=/usr/lib/php/20151012/xdebug.so




docker

https://linuxconfig.org/how-to-install-docker-on-ubuntu-20-04-lts-focal-fossa
https://docs.docker.com/get-started/

sudo chmod 666 /var/run/docker.sock
sudo apt  install docker-compose

touch docker-compose.yml

https://docs.docker.com/compose/compose-file/

https://docs.docker.com/engine/reference/builder/

docker-compose build




npm init
npm install express


npm run start
============================================================



pip3 freeze > requirements.txt
pip3 install -r requirements.txt





sudo apt install pipenv
pipenv run pip3 freeze > requirements.txt


http://www.iasptk.com/install-sphinx-ubuntu/
https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-sphinx-on-ubuntu-16-04




Можно собрать дистрибутив с нужным модулем.
Зайти в папку build
Выполнить команду:
php distro.php ../ 6.0
php patch.php ../ 6.0



composer dumpautoload -o


//\App\SiteControl\Service\NetcatProvider::getInstanceData($site);
//$this->getInstanceData();
 



https://www.youtube.com/watch?v=Zqts928j674
https://www.youtube.com/watch?v=XUMPI0daKTs 


echo "/usr/sbin/mysqld { }" > /etc/apparmor.d/usr.sbin.mysqld
apparmor_parser -v -R /etc/apparmor.d/usr.sbin.mysqld
systemctl restart mariadb
