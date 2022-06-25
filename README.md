![example workflow](https://github.com/kuzdmv/yamdb_final/actions/workflows/yamdb_workflow.yml/badge.svg)
# api_yamdb 
# Проект YaMDb
## Описание
Проект YaMDb собирает отзывы (Review) пользователей на произведения (Titles). Произведения делятся на категории: «Книги», «Фильмы», «Музыка». Список категорий (Category) может быть расширен администратором (например, можно добавить категорию «Изобразительное искусство» или «Ювелирка»).
Сами произведения в YaMDb не хранятся, здесь нельзя посмотреть фильм или послушать музыку.
В каждой категории есть произведения: книги, фильмы или музыка. Например, в категории «Книги» могут быть произведения «Винни-Пух и все-все-все» и «Марсианские хроники», а в категории «Музыка» — песня «Давеча» группы «Насекомые» и вторая сюита Баха.
Произведению может быть присвоен жанр (Genre) из списка предустановленных (например, «Сказка», «Рок» или «Артхаус»). Новые жанры может создавать только администратор.
Благодарные или возмущённые пользователи оставляют к произведениям текстовые отзывы (Review) и ставят произведению оценку в диапазоне от одного до десяти (целое число); из пользовательских оценок формируется усреднённая оценка произведения — рейтинг (целое число). На одно произведение пользователь может оставить только один отзыв.

### Технологии
- Python 3.8
- Django 2.2.19
- DRF, JWT
### Запуск проекта в dev-режиме
- Установите и активируйте виртуальное окружение
- Установите зависимости из файла requirements.txt
```
pip install -r requirements.txt
``` 
- В папке с файлом manage.py выполните команду:
```
python3 manage.py runserver
```
- Документация проекта доступна по адресу:
```
http://localhost/redoc/
```
### Распределение задач в команде

- Первый разработчик пишет всю часть, касающуюся управления пользователями (Auth и Users): систему регистрации и аутентификации, права доступа, работу с токеном, систему подтверждения через e-mail.
- Второй разработчик пишет категории (Categories), жанры (Genres) и произведения (Titles): модели, представления и эндпойнты для них.
- Третий разработчик занимается отзывами (Review) и комментариями (Comments): описывает модели, представления, настраивает эндпойнты, определяет права доступа для запросов. Рейтинги произведений тоже достаются третьему разработчику.

### Авторы проекта:
- Александр Соловьёв - автор первой части. 
https://github.com/haus2100
- Дмитрий Кузнецов - автор второй части.
https://github.com/kuzdmv
- Лев Белов - автор третий части.
https://github.com/WhiteLev

### Развернутый проект будет доступен по ссылке:
```
http://62.84.121.38/
http://62.84.121.38/admin/
```
