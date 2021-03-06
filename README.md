# Установка

```sh
$ git clone https://github.com/platonovAlexey/startuem.git #название папки
$ cd #название папки
$ npm install
$ bower install
```

#### Инструкции по проектру
	- Сборка предназначена для "новых"" браузеров IE10+
	- Создана структура сайта, все разбито по папкам
	- gulp-rigger — киллер фича. Плагин позволяет импортировать один файл в другой простой конструкцией //=
	- Для спрайтов использован плагин gulp.spritesmith - чтобы все заработало в консоли нужно прописать команду **gulp sprite** путь в миксинах sprite.scss background-image: url(/img/sprites/#{$sprite-image})
	- Подключен favicon
	- Вшит **normalize.css**
	- Подключены стили и скрипты
	- Шрифты нужно генерировать через [белку], файлы уже подключены
	- Добавлена функция, которая переводит px в em example:em(16px),если нужно для отдельного тега сделать line-height, то писать через !important
	- Добавлены переменные font-size/line-height для body


#### Структура

```sh
#### src
	├──fonts
	├  	├──папки с шрифтами
	├──js
	├  ├──partials #папка с скриптами
	├  			├── app.js
	├  ├──main.js #файл где подключаются скрипты и библиотреки
	├──img
	├		├──bg #фон, паттерн
	├		├──icons #иконки - отсюда берутся иконки для спрайта (подпапки)
	├		├──logos #логотипы
	├		├──sprites #спрайт - сборка (тут так же лежит файл scss)
	├		├──other #динамический контент
	├──styles
	├		├──helpers #папка с файлами миксинов и переменных, а так же normalize
	├		├──sections #папка для стилизации секций (header,footer, etc)
	├		├──main.scss #import всех scss файлов
	├──template #папка с шаблонами импортированых файлов (//=)

```

#### Разработка

```sh
$ gulp html:build - отдельно собирает html;
$ gulp js:build - отдельно собирает js;
$ gulp style:build - отдельно собирает css;
$ gulp fonts:build - отдельно собирает fonts;
$ gulp image:build - отдельно собирает image;
$ gulp sprite - собирает спрайт(использовать отдельно, указать путь в scss - /img/sprites/#{$sprite-image});
$ gulp build - собирает проект-продакшн в папку build;
$ gulp clean - удаляет папку build;
$ gulp - собирает проект, запускает сервер;
```

[белку]: <http://www.fontsquirrel.com/tools/webfont-generator>