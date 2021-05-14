Php-Storm
====================================

### Добавить проект
1. Creat new project from exsiting file
1. A folder with source files is added to project, server synchronization can be set up later
1. Выбрать папку docs проекта, нажать project root.
1. Сделать Excluded (исключает проект из индекса IDE) для следующий директорий
	- bitrix (все кроме modules)
	- upload

### Deploy

Tools → deployment → browse remote host

Тут же про сравнение файлов

### Горячие клавиши

File → Settings → Keymap

Плагин ```key promouter``` - напоминает о горячих клавишах

### Подсказки/сниппеты

File → Settings → Editor → liveTemplates

[https://github.com/matiaspub/bxCompSnpt](https://github.com/matiaspub/bxCompSnpt)

[пример](http://habrastorage.org/storage3/742/4cc/9c1/7424cc9c1d4026f07d3a39cd575bd91b.png)

### Инспектор кода

Стандартное использование: Code → InspectCode

Статья для продвинутых [http://stfalcon.com/blog/post/phpstorm-refactoring](http://stfalcon.com/blog/post/phpstorm-refactoring)

### Прочие фишки

BitirxApi - [https://dev.1c-bitrix.ru/community/webdev/user/156743/blog/9382/](https://dev.1c-bitrix.ru/community/webdev/user/156743/blog/9382/)

Общая статья о полезных функция PhpStorm - [https://habrahabr.ru/post/212077/](https://habrahabr.ru/post/212077/)

### Настройка SASS

1. Установить [http://rubyinstaller.org/](http://rubyinstaller.org/)
2. В консоли Ruby запустить: gem install sass
3. В PhpStorm произвести настройки - [http://www.angarsky.ru/sites/default/files/blog-images/2013-12-10_0023.png](http://www.angarsky.ru/sites/default/files/blog-images/2013-12-10_0023.png)
4. Для поддержки русских символов необходимо к аргументам добавить **-E utf-8**

### Общие настройки форматирования

Применить общие настройки форматирования, для этого скачать файл [settings.jar](data/settings.jar)

1. File → ImportSettings
2. Загрузить настройки
3. File → DefaultSettings → Editor → CodeStyle - выбрать Scheme - **Prioritet**
4. File → Settings → Editor → CodeStyle - проверить, что выбрана Scheme - **Prioritet**

Пользоваться **Ctrl+Alt+L** на своих проектах, чтобы форматирование у всех было единым

Использовать New-PHPClass/PhpFile/PhpIblockFile c готовыми шапками

Изменить шапку в создаваемом документе File → Editor → File and Code Templtes

Сделать подсветку строк по двойному клику [https://toster.ru/q/64490](https://toster.ru/q/64490)