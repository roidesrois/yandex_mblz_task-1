# Яндекс мобилизация 2017. Тестовое задание №1 в ШРИ.

## Задача:
Сверстать расписание лекций проекта «Мобилизация» для всех трёх школ.
[Подробное описание задания](https://academy.yandex.ru/events/frontend/shri_msk-2017/)

[Live demo](https://roidesrois.github.io/)

## Реализация:
Создана страница с расписанием лекций проекта «Мобилизация». Страница адаптивная и корректно отображается в современных версиях Яндекс.Браузера, Google Chrome, Firefox, Safari и Opera, а также в IE11+.

В расписании указано следущее:

* школа, для которой читается лекция (или несколько школ для общих лекций)
* тема лекции
* имя лектора
* дополнительная информация о лекторе
* дата и время проведения лекции
* место проведения лекции

Сначала в расписании отображаются еще предстоящие лекции, отсортированные по дате. Лекции, которые уже прошли, помечены соответствующим образом. Для них доступна ссылка на материалы.

Реализована фильтрация по школам, датам и аудиториям.

Данные о лекциях берутся из файла `./src/js/schedule-data.js`

Для удобства в разработке использовались следующие инструменты:

* Шаблонизатор mustache.js
* Препроцессор sass (+ дополнительные модули autoprefixer, clean-css, imagemin и др)
* Сборщик gulp 4.5

А также был выбран небольшой плагин Pikaday.js  для подключения кастомного календаря.   
Причина: Safari и Firefox не поддерживают текстовое поле type='date', а в остальных браузерах контролы выглядят по разному.
