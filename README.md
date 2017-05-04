Лекции для Android стажировки

## Создание лекций

1. В корне проекта создать копию `example.html` и назвать её `lecture ## - Android - name.html`
1. Добавить ссылку на этот файл в `index.html`
1. Добавить матеиралы лекции
1. Для медиа файлов и изображений необходимо создать свою директорию в `/lecture/...`

Редактировать лекции можно двумя способами: Markdown Style и HTML Style.

* HTML добавляется к файлу лекции как есть, прямо в тэги `<section>`. Этот способ более гибкий и подходит для сложных слайдов
* Markdown добавляется как в тэги напрямую, так в отдельные *.md-файлы. Внешние *.md-файлы необходимо размещать в `/lecture/...`
* Лекции построены на базе фреймворка [Reveal.js](https://github.com/hakimel/reveal.js)
* [Reveal.js shortcuts](https://github.com/hakimel/reveal.js/wiki/Keyboard-Shortcuts)
* Кроме документации можно посмотреть на примеры из `example.html`

Фреймворк был расширен. Доступны следующие css-классы.
* `.half-left`, `.half-right` для разделения слайда на 2 части
* `.third-left`, `.third-center`, `third-right` на 3 части
* `.underfloating` необходимо добавить к блоку под колонками, чтобы добиться правильного позиционирования.
* `.center` — центрирование по высоте, `.center-horizontal` — центрирование по ширине. Можно использовать как для `<section>`, так и для контента вашего блока
* `.tiny`, `.small`, `.large` — для блока `<code>`, чтобы разместить большой листинг и сделать акцент на одной строчке
* Мелкие участки кода можно приблизить с помощью `Alt` + `mouseclick`. Клик по слову — увеличит слово. Клик по области рядом — увеличит абзац

## Запуск лекции

Вообще html страничка запустится и без всяких скриптов. Если вся верстка находится в html — заработает без проблем, если же верстка находится во внешних markdown файлах в директорри lecture — тогда необходимо запустить локальный сервер.

1. Инициализировать зависимости — `npm install` — один раз для проекта
1. Запустить сервер — `npm start -- --port=8000`
    * Сервер запустится по адресу localhost:8000
    * Все изменения автоматически трекаются и появляются если обновить страницу презентации
    * Можно разрабатывать и сразу смотреть, что получается
1. Все готово? push в master
1. Через минуту лекции доступны в публичном доступе на [Github Pages](https://noveogroup.github.io/university-android-presentations/)

## Экспорт лекций в pdf

* Открыть лекцию через Google Chrome и добавить к адресу `...lecture.html?print-pdf`
* нажать `Ctrl` + `P` и выбрать сохранение в PDF

## Добавление Speaker Notes

Специальный режим для спикера открывается по клавише `s`. т.к. лекции в публичном доступе — заметки могут прочитать все желающие, будьте аккуратней в своих формулировках :)

* в HTML заметки добавляются через тэг `<aside class="notes">`. Можно добавить атрибут `data-markdown` для оформления заметки
* в Markdown заметки добавляются после строчки `Note:`, изменить этот маркер можно через атрибут `data-separator-notes=""`
* подробнее в [документации](https://github.com/hakimel/reveal.js/#speaker-notes)

## Установка NPM

1. Скачать `npm`
    * прописать путь до него в PATH
1. Скачать grunt-cli — `npm install -g grunt-cli`
