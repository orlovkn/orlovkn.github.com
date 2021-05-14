### Установка
```
composer create-project symfony/website-skeleton mysite.local
```

[install](htps://www.youtube.com/watch?v=ABdeoIm6e74)

[дока](https://symfony.ru/doc/current/doctrine.html)

### создать сущность
```
php bin/console make:entity
```
С67С
### создать новую миграцию
```
php bin/console make:migration
```

### опросить на предмет изменений в сущностях
```
php bin/console doctrine:migrations:diff
```

### выполнить существующие миграции
```
php bin/console doctrine:migrations:migrate
```

```
To run just this migration for testing purposes, you can use migrations:execute --up 'DoctrineMigrations\\Version20201027035620'

To revert the migration you can use migrations:execute --down 'DoctrineMigrations\\Version20201027035620'
```

### очистить кэш
```
bin/console cache:clear
```

### создать пользователя
```
bin/console make:user
```
### сделать аутентификацию
```
bin/console make:auth
```

### хз
```
php bin/console messenger:consume async
```



https://websiteforstudents.com/how-to-install-symfony-5-on-ubuntu-18-04-16-04-with-nginx/



### создать контроллер
php bin/console make:controller
php bin/console make:controller NameOfController


### создать базу
php bin/console doctrine:database:create

### роутинг
php bin/console debug:router

### создать форму
bin/console make:form
https://symfony.com/doc/current/forms.html

### поля
update_at — datetime
is_published — boolean
ManyToOne — relationship

Main types
  * string
  * text
  * boolean
  * integer (or smallint, bigint)
  * float

Relationships / Associations
  * relation (a wizard 🧙 will help you build the relation)
  * ManyToOne
  * OneToMany
  * ManyToMany
  * OneToOne

Array/Object Types
  * array (or simple_array)
  * json
  * object
  * binary
  * blob

Date/Time Types
  * datetime (or datetime_immutable)
  * datetimetz (or datetimetz_immutable)
  * date (or date_immutable)
  * time (or time_immutable)
  * dateinterval

Other Types
  * ascii_string
  * decimal
  * guid
  * json_array



```
$patchList = $this->patchRepository->findBy([], ['id' => 'DESC'], 5, 0);

$repository = $this->getDoctrine()
                   ->getManager()
                   ->getRepository('GeneralRegistrationBundle:Service');

$service = $repository->findOneBy(array('name' => 'Registration'),array('name' => 'ASC'));

$comment = $service->getComment();
$name = $service->getName();

return new Response('le service is '. $name . ', content is ' . $comment);
```

```
$service = $repository->findBy(array('name' => 'Registration'),array('name' => 'ASC'),1 ,0);
$repository->findBy(array('name' => 'Registration'),array('name' => 'ASC'),1 ,0)[0];
```

https://folkprog.net/doctrine-symfony-framework/


### сервисы
выполняют только логику

### Ссылки


### Список всех команд в указанном пространстве имен
bin/console list make


```
public function index(Request $request)
{
    $greet = '';
    if ($name = $request->query->get('hello')) {
        $greet = sprintf('<h1>Hello %s!</h1>', htmlspecialchars($name));
    }
```

про создание базы
https://symfonycasts.com/screencast/symfony-doctrine/docker-database#play

```
DATABASE_URL=postgresql://127.0.0.1:5432/db?serverVersion=11&charset=utf8
```


### админки
https://symfony.com/doc/current/bundles/EasyAdminBundle/index.html
https://symfony.com/doc/current/cmf/tutorial/sonata-admin.html

### установка easy admin
```
composer req admin
composer require easycorp/easyadmin-bundle
```

конфигурация дашборда
https://symfony.com/doc/current/bundles/EasyAdminBundle/dashboards.html

установка дашбоарда
```
bin/console make:admin:dashboard
```

конфигурация crud
https://symfony.com/doc/current/bundles/EasyAdminBundle/crud.html


```
$commentRepository->findBy(['conference' => $conference], ['createdAt' => 'DESC']),
```

```
comment.createdAt|format_datetime('medium', 'short')
```

```
{% if comments|length > 0 %}
{% for comment in comments %}
{% endfor %}
{% else %}
<div>No comments have been posted yet for this conference.</div>
{% endif %}
```

```
<a href="{{ path('conference', { id: conference.id }) }}">View</a>
```

Функции и фильтры Twig доступные только в Symfony;
https://symfony.com/doc/current/reference/twig_reference.html

```
return $this->findBy([], ['year' => 'ASC', 'city' => 'ASC']);
```

## список запущенных мессенджеров
php bin/console debug:messenger

## пересмотреть список мессенджеров
sudo supervisorctl start messenger-consume:*

## установка транспортов
php bin/console messenger:setup-transports


## тестирование
https://symfony.com/doc/current/testing.html


composer req phpunit


php bin/phpunit

https://www.youtube.com/watch?v=HA3NfbjRsX0

https://symfony.com/doc/current/components/phpunit_bridge.html

https://symfony.com/doc/current/testing.html#your-first-functional-test

./vendor/bin/simple-phpunit


Создадим тест с помощью бандла maker:
```
bin/console make:functional-test Controller\\ConferenceController
```

Запустите новые тесты только для этого класса:
```
bin/phpunit tests/Controller/ConferenceControllerTest.php
```

тест, который щёлкает по любой ссылке конференции на главной странице:
```
public function testConferencePage()
{
    $client = static::createClient();
    $crawler = $client->request('GET', '/');
    $this->assertCount(2, $crawler->filter('h4'));
    $client->clickLink('View');
    $this->assertPageTitleContains('Amsterdam');
    $this->assertResponseIsSuccessful();
    $this->assertSelectorTextContains('h2', 'Amsterdam 2019');
    $this->assertSelectorExists('div:contains("There are 1 comments")');
}
```

отправка формы
```
public function testCommentSubmission()
{
    $client = static::createClient();
    $client->request('GET', '/conference/amsterdam-2019');
    $client->submitForm('Submit', [
        'comment_form[author]' => 'Fabien',
        'comment_form[text]' => 'Some feedback from an automated functional test',
        'comment_form[email]' => 'me@automat.ed',
        'comment_form[photo]' => dirname(__DIR__, 2).'/public/images/under-construction.gif',
    ]);
    $this->assertResponseRedirects();
    $client->followRedirect();
    $this->assertSelectorExists('div:contains("There are 2 comments")');
}
```

В тесте PHPUnit вы можете получить любой сервис из контейнера с
помощью метода self::$container->get() , который также даёт доступ
к непубличным сервисам.
```
// simulate comment validation
$comment = self::$container->get(CommentRepository::class)->findOneByEmail($email);
$comment->setState('published');
self::$container->get(EntityManagerInterface::class)->flush();
```


## Makefile
```
SHELL := /bin/bash
tests:
  bin/phpunit
.PHONY: tests
```
+ запуск
```
make tests
```

Переменная окружения SYMFONY_DEFAULT_ROUTE_URL содержит URL-
адрес локального веб-сервера.
```
$client = static::createPantherClient(['external_base_uri' => $_SERVER['SYMFONY_DEFAULT_ROUTE_URL']]);
```

Список проверок в Symfony для функциональных тестов;
https://symfony.com/doc/current/testing/functional_tests_assertions.html

дока PHPUnit
https://phpunit.readthedocs.io/ru/latest/index.html


Symfony-библиотека Panther для тестирования в браузере и парсинга сайтов в приложениях Symfony;
https://github.com/symfony/panther


```
return $this->createQueryBuilder('c')
    ->andWhere('c.conference = :conference')
    ->andWhere('c.state = :state')
    ->setParameter('conference', $conference)
    ->setParameter('state', 'published')
    ->orderBy('c.createdAt', 'DESC')
    ->setMaxResults($limit)
    ->setFirstResult($offset)
```

```
private const DAYS_BEFORE_REJECTED_REMOVAL = 7;

private function getOldRejectedQueryBuilder(): QueryBuilder
{
    return $this->createQueryBuilder('c')
                ->andWhere('c.state = :state_rejected or c.state = :state_spam')
                ->andWhere('c.createdAt < :date')
                ->setParameters([
                                    'state_rejected' => 'rejected',
                                    'state_spam' => 'spam',
                                    'date' => new \DateTime(-self::DAYS_BEFORE_REJECTED_REMOVAL . 'days'),
                                ]);
}
```

## Ассинхронность

отобразить логи обращения к мессенджеру
```
bin/console messenger:consume async -vv
```


прослушать дампы в консоли
```
bin/console server:dump
```

Учебный видеоролик по Webpack Encore на SymfonyCast.
https://symfonycasts.com/screencast/webpack-encore/encore-install


## работа с API
установка 
```
composer req api
```

включение поддержки graphql
```
composer require webonyx/graphql-php
```


https://symfonycasts.com/screencast/symfony/services#play

```
php bin/console debug:autowiring
php bin/console debug:autowiring log
```


## список запущенных мессенджеров
php bin/console debug:messenger

## пересмотреть список мессенджеров
sudo supervisorctl start messenger-consume:*

## установка транспортов
php bin/console messenger:setup-transports


################################
SUPERVISOR


sudo systemctl start supervisor
sudo systemctl enable supervisor
sudo systemctl status supervisor




messenger:consume --limit=10

messenger:stop-workers




[program:messenger-consume]
command=php /egov/www/controller/html/bin/console messenger:consume async --limit=1 --time-limit=3600
user=nginx
numprocs=1
startsecs=0
autostart=true
autorestart=true
process_name=%(program_name)s_%(process_num)02d



sudo supervisorctl reread

sudo supervisorctl update


    App\SiteControl\EventListeners\EntityLoggerEvents:
        arguments:
            $formatter: '@monolog.formatter.mongodb'
        tags:
            - { name: 'doctrine.event_listener', event: 'postPersist' }
            - { name: 'doctrine.event_listener', event: 'postUpdate' }
            - { name: 'doctrine.event_listener', event: 'preRemove' }



symfony console debug:container lexik_jwt_authentication.handler.authentication_failure


https://symfony.com/doc/current/setup/symfony_server.html#docker-integration