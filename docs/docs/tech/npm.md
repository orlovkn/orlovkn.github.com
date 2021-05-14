## Использование npm

Использование пакетного менеджера позволяет удобно и быстро подключать новые библиотеки для разработки, при этом не тратить ресурсы на загрузку разных файлов при загрузке страницы в браузере, потому что сборщик мимнимизирует файл и собирает его в один

### Установка

Создаем папку ```local/assets``` Переходим в нее и инициализируем npm
```
cd local/assets
npm init -y
```

Проверяем, что в папке создан файл ```local/assets/package.json```

Устанавливаем laravel-mix
```
npm install laravel-mix --save-dev
```

после чего добавится папка ```node_modules``` и файл ```package-lock.json```

Затем скопируем конфигурационный файл сборщика в корень нашей дирректории
```
cp node_modules/laravel-mix/setup/webpack.mix.js ./
```

### Сборка

Результирующие файлы поместим в папку ```/public``` и оттуда будем их подключать А все файлы с исходным кодом разместим в папке ```/local/assets/src/```, там будут лежать ```app.js``` и ```app.scss``` После того, как все файлы и папки созданы пропишем в ```webpack.mix.js```
```
mix.js('src/app.js', '../../public').sass('src/app.scss', '../../public').setPublicPath('../../public');
```

И установим пакет cross-env
```
npm install cross-env --save-dev
```

Далее разместим в ```package.json``` алиасы команд сборки
```
"scripts": {
    "dev": "npm run development",
    "development": "cross-env NODE_ENV=development node_modules/webpack/bin/webpack.js --progress --hide-modules --config=node_modules/laravel-mix/setup/webpack.config.js",
    "watch": "npm run development -- --watch",
    "hot": "cross-env NODE_ENV=development node_modules/webpack-dev-server/bin/webpack-dev-server.js --inline --hot --config=node_modules/laravel-mix/setup/webpack.config.js",
    "prod": "npm run production",
    "production": "cross-env NODE_ENV=production node_modules/webpack/bin/webpack.js --no-progress --hide-modules --config=node_modules/laravel-mix/setup/webpack.config.js"
  },
```

И запустим саму сборку
```
npm run dev
```

На этом все, в ```/public``` вы должны увидеть ```app.js``` и ```app.css``` Для примера установим jquery и bootstrap и соберем все
```
npm install popper.js
npm install jquery
npm install bootstrap
```

подключим пакет bootstrap в основной файл ```/local/assets/src/app.js```
```
require('bootstrap');
```

и повторим выполнение команды сборки
```
npm run dev
```

Итого, что должно получится на выходе

- ```/public``` - с файлами app.js и app.css
- ```/assets/node_modules``` - все установленные пакеты и зависимости
- ```/assets/src``` - файлы с исходным кодом, в нашем случае подключенный bootstrap и только
- ```/assets/package.json```

```
{
  "name": "assets",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "dev": "npm run development",
    "development": "cross-env NODE_ENV=development node_modules/webpack/bin/webpack.js --progress --hide-modules --config=node_modules/laravel-mix/setup/webpack.config.js",
    "watch": "npm run development -- --watch",
    "hot": "cross-env NODE_ENV=development node_modules/webpack-dev-server/bin/webpack-dev-server.js --inline --hot --config=node_modules/laravel-mix/setup/webpack.config.js",
    "prod": "npm run production",
    "production": "cross-env NODE_ENV=production node_modules/webpack/bin/webpack.js --no-progress --hide-modules --config=node_modules/laravel-mix/setup/webpack.config.js"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "devDependencies": {
    "cross-env": "^7.0.2",
    "laravel-mix": "^5.0.4",
    "resolve-url-loader": "^3.1.0",
    "sass": "^1.26.5",
    "sass-loader": "^8.0.2",
    "vue-template-compiler": "^2.6.11"
  },
  "dependencies": {
    "bootstrap": "^4.4.1",
    "jquery": "^3.5.0",
    "popper.js": "^1.16.1",
  }
}
```

- ```/assets/package-lock.json``` - файл хранит в себе версии установленных пакетов с целью соответствия их на разных окружениях
- ```/assets/webpack.mix.js```

```
let mix = require('laravel-mix');
mix.js('src/app.js', '../../public').sass('src/app.scss', '../../public').setPublicPath('../../public');
```

Далее вы можете устанавливать дополнительные библиотеки, писать свой код css и js в исходных файлах или в других, подключая в исходный при помощи require, использовать сборку для dev, production окружений, во время разработки запускать команду

```
npm run watch
```

которая будет обновлять сборку по мере изменения исходников

### links
- [laravel-mix](https://laravel-mix.com/docs/5.0/installation)