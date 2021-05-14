## composer

```
composer init
composer install
composer update
composer remove vendor/package
```


examples composer.json

```
{
	"extra": {
		"installer-paths": {
				"bitrix/modules/{$name}/": ["type:bitrix-module"]
			}
	},
	"require": {
		"andreyryabin/sprint.options": "dev-master",
		"arrilot/bitrix-migrations": "^2.3",
		"symfony/var-dumper": "^3.3"
	}
}
```

```
{
    "require": {
        "roave/security-advisories": "dev-master",
        "cjp2600/bim-core": "^1.1",
        "monolog/monolog": "^1.21",
        "symfony/config": "^3.1",
        "symfony/yaml": "^3.1",
        "symfony/dependency-injection": "^3.1",
        "mikehaertl/phpwkhtmltopdf": "^2.2",
        "mongodb/mongodb": "^1.1",
        "ocramius/proxy-manager": "^1.0",
        "symfony/proxy-manager-bridge": "^3.2",
        "symfony/expression-language": "^3.2",
        "symfony/validator": "^3.2",
        "php-amqplib/php-amqplib": "2.5.*",
        "symfony/symfony": "^3.2",
        "sensio/framework-extra-bundle": "^3.0",
        "sensio/distribution-bundle": "^5.0",
        "symfony/monolog-bundle": "^3.1",
        "box/spout": "^2.7",
        "phpoffice/phpspreadsheet": "1.0.0-beta"
    }
}
```

```
{
  "require": {
    "roave/security-advisories": "dev-master",
    "cjp2600/bim-core": "^1.1",
    "monolog/monolog": "^1.21",
    "symfony/config": "^3.1",
    "symfony/yaml": "^3.1",
    "symfony/dependency-injection": "^3.1",
    "mikehaertl/phpwkhtmltopdf": "^2.2",
    "mongodb/mongodb": "^1.1",
    "adv/osago-rsa": "^1.7",
    "adv/osago-kbm": "^0.1",
    "ocramius/proxy-manager": "^1.0",
    "symfony/proxy-manager-bridge": "^3.2",
    "symfony/expression-language": "^3.2",
    "symfony/validator": "^3.2",
    "php-amqplib/php-amqplib": "2.5.*",
    "symfony/symfony": "^3.2",
    "sensio/framework-extra-bundle": "^3.0",
    "sensio/distribution-bundle": "^5.0",
    "symfony/monolog-bundle": "^3.1",
    "box/spout": "^2.7",
    "phpoffice/phpspreadsheet": "1.0.0-beta"
  },
  "autoload": {
    "psr-4": {
      "Adv\\": "local/php_interface/adv/lib"
    }
  },
  "repositories": [
    {
      "type": "vcs",
      "url": "git@scm.adv.ru:/sgz/osago-rsa.git"
    },
    {
      "type": "vcs",
      "url": "git@scm.adv.ru:/sgz/osago-kbm.git"
    }
  ]
}
```

```
{
  "require": {
    "slim/slim": "4.*",
    "nyholm/psr7": "^1.3",
    "nyholm/psr7-server": "^1.0",
    "guzzlehttp/psr7": "^1.6",
    "http-interop/http-factory-guzzle": "^1.0",
    "laminas/laminas-diactoros": "^2.4",
    "tuupola/slim-basic-auth": "^3.2"
  },
  "autoload": {
	"psr-4": {
	  "Api\\App\\": "app"
	}
  }
}

```


```
"autoload": {
    "classmap": [
        "services/myserv/Ksl.php"
    ],
    "psr-4": {
        "Services\\": "services",
        "liw\\": ""
    },
    "files": [
        "config.php"
    ]
}
```

```
composer dump-autoload -o
```

```
{
    "name": "manuelgil/rest-api-with-slim-php",
    "description": "REST API with PHP Slim Framework 3 and MySQL",
    "version": "1.0.0.8",
    "type": "project",
    "license": "MIT",
    "authors": [
        {
            "name": "Manuel Gil",
            "email": "atencion.ms@outlook.com",
            "role": "Developer"
        }
    ],
    "require": {
        "php": ">=5.6.4",
        "monolog/monolog": "^1.25",
        "phpmailer/phpmailer": "^6.1",
        "slim/http-cache": "^0.4.0",
        "slim/slim": "^3.12",
        "tuupola/slim-jwt-auth": "^2.4",
        "vlucas/phpdotenv": "^2.6"
    },
    "support": {
        "issues": "https://github.com/ManuelGil/REST-Api-with-Slim-PHP/issues",
        "source": "https://github.com/ManuelGil/REST-Api-with-Slim-PHP"
    },
    "autoload": {
        "files": [
            "src/config/config.php"
        ],
        "classmap": [
            "src/libs"
        ]
    },
    "minimum-stability": "stable",
    "config": {
        "preferred-install": "dist",
        "optimize-autoloader": true,
        "sort-packages": true
    }
}
```

#### links

- [хабр](http://habrahabr.ru/post/145946/)