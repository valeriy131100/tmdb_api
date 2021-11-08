# tmdb_api
Набор утилит для обращения к The Movie Database и локальной работы с её копией.

# hello_api_TMDB.py
Скрипт предназначен для проверки работоспособности вашего API-ключа к TMDB.

Просит пользователя ввести API-ключ и пытается вывести бюджет фильма с номером 215.

В случае неудачи выводит "Invalid api key", в противном случае выводит бюджет.

# make_own_db.py
Скрипт предназначен для создания локальной копии базы данных TMDB.

Просит пользователя ввести API-ключ, в случае если ключ неработоспособен, то выводит сообщение "Invalid api key". В противном случае создает копию первой тысячи фильмов на TMDB под названием MyFilmDB.json.

# search_in_db.py
Скрипт предназначен для поиска по локальной копии базы данных TMDB.

Просит пользователя указать путь до базы данных, предположительно, ранее созданой [make_own_db.py](#make_own_dbpy). В случае неудачной попытки найти базу данных по заданному пути выводит "File not found, sorry...".

В противном случае просит пользователя ввести запрос для поиска по базе данных и в ответ выводит найденные фильмы.

# find_similar.py
Скрипт предназначен для поиска фильмов схожих с фильмом заданным пользователем. Поиск идет среди локальной копии базы данных TMDB.

Просит пользователя указать путь до базы данных, предположительно, ранее созданой [make_own_db.py](#make_own_dbpy). В случае неудачной попытки найти базу данных по заданному пути выводит "File not found, sorry...".

Далее просит пользователя указать фильм, по которому он хотел бы получить рекомендации. Если подобного фильма нет в базе данных, то выводит "No such film in FilmsDB". В противном же случае программа выводит 8 фильмов, которые наиболее схожи с введенным пользователем.

Фильмы оцениваются на схожесть по вхождению в коллекции, языку, бюджету и жанрам.

# tmd_helpers.py
Файл содержит набор функций для удобной работы с TMDB API.

Реализует обращение к методам API TMDB, получение json с заданного url, а также получение API-ключа от пользователя.

# own_db_helpers.py
Файл содержит набор функций для удобной работы с локальной копией базы данных TMDB.

Реализует загрузку базы данных из файла по заданному пути.
