# Расширение для «Универсального редактора»

Директива к «Универсальному редактору» котрорая расширяет возможности рендактора, добавляя поле wysiwyg.

## Установка расширения

Данное расширение подтягивается как bower зависимость. Для подключения расширения в проект требуется выполнить
следующую команду, находясь в корневой директории проекта:

* bower install https://github.com/universal-editor/tinymce-plugin --save -F
* требуется произвести подлкючение javascript - файла, css файла:
  * tinymce-plugin.min.js - основной файл расширения у-редактора.
  * tinymce-plugin.min.css - файл стилей расширения у-редактора.
* само расширение использует библиотеку tinymce-dist, для которой требуются файлы находщисеся в каталоге mce-files

Подключение модуля:
```javascript
    angular.module('unEditor',['tinymce.plugin']);
```

Для корректной работы расширения у-редактора требуется набор дополнительных библиотек, расширяющих функционал AngularJS.
Актуальный список библиотек и их версий доступены в файле bower.json данного репозитория в "разделе" dependencies. Если
расширение подключать через bower, то он сам скачает нужные библиотеки.

Пояснение:

Желательно при сборке проекта, в котором подключается данное расширение, использовать gulp плагины :
* main-bower-files - собирает пути для всех библиотек указанных в bower.json
* gulp-inject - может подключать js и css в проект в указанном месте

## Документация

* [Поле tinymce](docs/tinymce.md)