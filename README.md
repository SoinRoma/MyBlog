# Blog

Для запуска  проекта понадобится локальный сервер OpenServer, который нужно запускать заранее. В нём нужно сделать следущее:
+ В настройках основных сделать автозапуск сервера и требовать Администратора постоянно.
+ В настройках кодировки выбрать utf-8 и utf-8_general_ci
+ В домменах добавить папки с сайтами, которые будут использоваться.

Затем нужно создать папку в \OpenServer\domains , где будет лежать проект. Открываем эту папку через PhpStorm и делаем следующее:
+ Заходим в Settings\Languages&Frameworks\PHP и выбираем версию PHP (не ниже 7.1)
+ И путь интерпретатора (\OpenServer\modules\php\PHP_7._)

Установка Laravel в проект:
+ Заходим в OpenServer и бывираем консоль
+ Переходим в консоли к папке \OpenServer\domains 
+ Для начала обновить композер composer self-update
+ Вводим для установки Laravel composer create-project laravel/laravel ИмяПапки

Установка полезных плагинов:
+ В самом PhpStorm установить плагин Laravel
+ Установить Laravel DebugBar в папке проекта через консоль: composer require barryvdh/laravel-debugbar --dev
+ В проекте в config/app.php прописать в конце: Barryvdh\Debugbar\ServiceProvider::class,
+ Проверить, что в файле .env: APP_DEBUG=true
+ Установить Laravel Ide-helper: composer require --dev barryvdh/laravel-ide-helper
+ В проекте в config/app.php прописать в конце: Barryvdh\LaravelIdeHelper\IdeHelperServiceProvider::class,
+ Затем в консоле: php artisan ide-helper:generate
