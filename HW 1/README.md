# 2024-Database-systems 1 задание
Homework and materials for the Database Systems course

## Отчет

### Установка Mongo и запуск в Docker

Docker у меня уже был установлен ранее, я создал кофиг для Docker Compose `MongoDocker.yml`, и запустил этот файл командой:

```
docker-compose -f .\MongoDocker.yml up -d
```
![Mongo в Docker](Скриншоты/Docker_запуск_контейнеров.png)

Взаимодействовать можно с помощью mongo-express, MongoDB Compass и mongosh.

<p align="center">
  <img src="Скриншоты/Подключился_по_localhost.png" alt="Описание изображения 1" width="45%"/>
  <img src="Скриншоты/Обмазались_монгой.png" alt="Описание изображения 2" width="45%"/>
</p>

### Начао работы с mongo через mongosh

Создать базу данных и переключится на нее можно с помощью команды`use`. Посмотреть не пустые базы данных можно с помощью `show dbs`. Создаем колекцию с помощью `db.createCollection` а посмотреть колекции `show collections`. MongoDB написана на C++ и в ней можно исполнять код, наример `print("Hi everyone!")`
![Начало работы](Скриншоты/stats.png)