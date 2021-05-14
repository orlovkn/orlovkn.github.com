jupyter-lab

ncdu /

sudo apt autoclean
sudo apt clean
sudo apt autoremove


идём в меню «Система» — «Параметры» — «Клавиатура»
окно с настройками открылось? идём во вкладку «Раскладки»
жмём на кнопку «Параметры»
ищем пункт «Клавиша для выбора 3его уровня». Выбираете привычную вам клавишу. Я выбрал по аналогии «Правая клавиша Alt»
ищем пункт «Разные параметры совместимости». Включаем пункт «Включить дополнительные типографские символы»



sudo subl /etc/hosts



sudo systemctl enable cron
# Cron Status
sudo systemctl status cron

*/15 * * * * /usr/bin/php /media/orlovkn/work/www/upd.gosweb.loc/cron/publish.php

https://www.digitalocean.com/community/tutorials/how-to-use-cron-to-automate-tasks-ubuntu-1804


crontab -e



sudo ufw enable


https://www.howtoforge.com/tutorial/install-apache-with-php-and-mysql-on-ubuntu-18-04-lamp/




sudo systemctl stop nginx
sudo systemctl start nginx
sudo systemctl restart nginx
sudo systemctl reload nginx
sudo systemctl status nginx

$ sudo systemctl start php7.0-fpm.service
$ sudo systemctl stop php7.0-fpm.service
$ sudo systemctl restart php7.0-fpm.service # <- restart it
$ sudo systemctl reload php7.0-fpm.service # <- reload it

sudo service php7.4-fpm restart




https://www.digitalocean.com/community/tutorials/mysql-ru

CREATE USER 'gosweb'@'localhost' IDENTIFIED BY '12345';
GRANT ALL PRIVILEGES ON * . * TO 'gosweb'@'localhost';



sudo subl /etc/nginx/sites-available/sym.loc

sudo ln -s /etc/nginx/sites-available/sym.loc /etc/nginx/sites-enabled/



[05.10.20 16:28]
ну там есть уже контроллеры

[05.10.20 16:28]
там есть такой класс NetcatProvider

[05.10.20 16:29]
в нем надо сделать методы которые будут забирать данные

[05.10.20 16:29]
использовать для запросов https://symfony.com/doc/current/http_client.html

[05.10.20 16:30]
дальше сделать в контроллере src/Controller/Api/V1/Site/SiteController.php

[05.10.20 16:30]
дополнительный метод для получения статистики

[05.10.20 16:30]
который будет в себе вызывать уже методы из NetcatProvider

[05.10.20 16:31]
дальше дергать метод контроллера в SiteDetail.vue

[05.10.20 16:35]
команды тут package.json


composer dump-autoload
composer dump-autoload -o


chmod -R a+rwx /var/www/mysite

chmod -R a+rwx /home/sys.local/konstantin.orlov/gosweb.gosuslugi.ru


https://serveradmin.ru/ustanovka-i-nastrojka-nginx/


echo "/usr/sbin/mysqld { }" > /etc/apparmor.d/usr.sbin.mysqld
apparmor_parser -v -R /etc/apparmor.d/usr.sbin.mysqld
systemctl restart mariadb


sudo ln -s /etc/apparmor.d/usr.sbin.mysqld /etc/apparmor.d/disable/

sudo apparmor_parser -R /etc/apparmor.d/usr.sbin.mysqld

It also disables the AppArmor for MySQL on the system though.


chown -R nginx:nginx ./
chown -R gosweb:gosweb ./


создать файл с ключами
$ htpasswd -c /etc/nginx/.htpasswd user1

server {
    ...
    location / {
        auth_basic "Restricted Area";
        auth_basic_user_file /etc/nginx/.htpasswd;
        ...
    }
}

    class: App\Formatter\MongoDB

sudo chmod -R a+rwx nginx:nginx /var/www/gosweb.loc/var/cache/dev/doctrine



chmod 755 /egov/www/updater/html/deploy.sh

sudo chmod -R a+rwx  /home/sys.local/konstantin.orlov



private function vlog($data, $file = '')
{
    if (!$file) {
        $file = 'log.txt';
    }
    $file = $_SERVER['DOCUMENT_ROOT'] . (substr($_SERVER['DOCUMENT_ROOT'], -1) == '/' ? '' : '/') . $file;
    $text = "----------------" . date('Y-m-d H:i:s') . "----------------\n";
    $text .= print_r($data, true);
    $text .= "\n\n";

    if ($fh = fopen($file, 'a')) {
        fwrite($fh, $text);
        fclose($fh);
    }
}

tar xvzf netcat-extra-6.0.0.20357-ok_activation_for_distr.tgz
tar xvzf 20201223142814_dev.gosweb.sitemanager.ru_full_GOpKf.tgz

php make_site_tgz.php gosweb_school_main
php distro.php ../ 6.0 extra
php distro.php ../ 6.0 extra --gosweb --no-archives


action:4
format:json
host:localhost
user:gosweb
dbname:restore
pass:12345
pwd:12345
demodistr:extra
custom_system_components:true


action:5
format:json
* 



$table = nc_db_table::make($record_table, 'Message_ID');

$db = nc_db();
$existing_record_id = $db->get_var(
    "SELECT Message_ID
       FROM $record_table
      WHERE (SystemName = 0 OR SystemName IS NULL)
        AND Version='" . $db->escape($current_version) . "'"
);

if ($existing_record_id) {
    $table->where_id($existing_record_id)->update($values);
}
else {
    $table->insert($values);
}



переназначить версию php
sudo update-alternatives --config php




sudo service mongodb stop 
sudo rm /var/lib/mongodb/mongod.lock 
sudo mongod --repair --dbpath /var/lib/mongodb 
sudo mongod --fork --logpath /var/lib/mongodb/mongodb.log --dbpath /var/lib/mongodb 
sudo service mongodb start



http://prodcontroller.goswebcms.ru/api/v1/site/update_all


git remote -v
git remote remove origin
git remote add origin https://gitlab.com/antontuzlukov/gosweb-controller.git
git fetch --all



composer require "doctrine/mongodb-odm"




Ich heiße... (My name is ...)
Wie heißt du? (What's your name?)
Freut mich! (Nice to meet you!)
Freut mich auch! (Nice to meet you, too!)

Gut gemacht! (Well done!)




dependencies:
  pre:
    - pecl channel-update pecl.php.net
    - pecl install -f redis


You should add "extension=redis.so" to php.ini



<router-link :to="/">123</router-link>



                    $tables[] = array_map(function ($item) {
                        return $item;
                    }, $this->modulesTables[$module['Keyword']]);


git remote -v
git remote remove origin
git remote add origin http://git.gosuslugi.local/gosweb-2/cms-netcat-gosweb.git



git remote add gitlab https://gitlab.com/orlovkn/cms-netcat-gosweb.git



php -S localhost:8000 -t public

Hello, 

My name is Konstantin and I am a backend web developer with 10+ years of experience in creating websites, different services, and so on.

During my work, I've been mostly working with PHP and also learned Python and Java. I love to learn new technologies or languages, and I pick up on new concepts fast, especially in a hands-on environment. I'm definitely and absolutely passionate about Clean code principles, SOLID, Design patterns. I like to write clean, understandable, and reusable code.

In my current work, I code on PHP and use the Symfony framework. Moreover, I've been using VueJS, Docker, Slim, Rest API, MySQL, Mongo, Redis, Selenium, RabbitMQ, and a bit AWS. Also, In my job, I prefer to use Linux based system to work more with the console and to understand better all procedures.

I’m highly interested in your Senior PHP Engineer position and I'm pretty sure I can be a good extension of your team.



аннотации
composer require doctrine/annotations


ssh root@10.81.18.3
YGbv8411

ssh konstantin.orlov@sys.local@10.81.18.3



git pull origin master
composer install
php bin/console doctrine:migrations:migrate -q
php bin/console cache:clear
php bin/console cache:warmup
systemctl restart supervisord
chown -R nginx:nginx ./


### ec2
sudo yum install httpd
sudo service httpd start
chkconfig on


https://www.youtube.com/watch?v=AtEqbYTLHfs

systemctl list-units
systemctl list-units |grep .service


npm list webpack

npm install -g n && n stable


    public const FIELDS = [
//        "FIELDS" => 'Поля формы',
        "UF_PRODUCT_CATEGORIES" => 'Категории товаров',
        "UF_PRICE_FROM" => 'Цена товара от',
        "UF_PRICE_TO" => 'Цена товара до',
        "UF_IS_MEDICINAL_PRODUCT" => 'Лекарственный препарат и БАД',
        "UF_FEED_NAME" => 'Имя файла',
    ];


array_keys($fields)



        $lastExportDate = $this->loyaltyExportRepository->findBy(
            ['UF_SENT' => 1],
            ['UF_DATE' => 'DESC'],
            1
        )->first();


    /**
     * @var PDO
     */
    private $connection;

    public function __construct(
        CatalogSettings $catalogSettings,
        OperatingBalancesFileService $operatingBalancesFileService
    )
    {
        $this->filesystem         = new Filesystem();
        $this->remainsInPath      = $catalogSettings->getRemainsInPath();
        $this->remainsArchivePath = $catalogSettings->getRemainsArchivePath();
        $this->operatingBalancesFileService = $operatingBalancesFileService;
        $this->makeConnection();
    }


    private function makeConnection(): void
    {
        try {
            $conn = Application::getInstance()->getConnectionPool()->getConnection('default')->getConfiguration();
            $this->connection = new PDO(
                'mysql:dbname='.$conn['database'].';host='.$conn['host'], $conn['login'], $conn['password']
            );
        } catch (PDOException | SystemException $e) {
            echo 'Подключение не удалось: ' . $e->getMessage();
            throw new ConnectionException('Не удалось установить соединение с базой данных.', $e->getCode(), $e);
        }
    }


just something to be aware of


$env = getenv('APP_ENV') ?? $_SERVER['APP_ENV'] ?? $_SERVER['HTTP_APP_ENV'] ?? self::PROD;


skifia.myjino.ru
skifia_orlov
m08blFgq%Wx7s$