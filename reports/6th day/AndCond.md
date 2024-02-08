# ***Работа с СУБД PostgreSQL:***
## *Создание таблицы:*
**CREATE TABLE** *Users*

+ (
  ID **INT** **PRIMARY KEY**,
  name **VARCHAR**(20), surname **VARCHAR**(30), age **SMALLINT**, gender **VARCHAR**(1)
  )

## *Добавление данных в таблицу:*

+ **INSERT INTO** *users* (ID, name, surname, age, gender) **VALUES** (1, 'Andrewl', 'Ivanov', 20, 'm')

+ **INSERT INTO** *users* (ID, name, surname, age, gender) **VALUES** (2, 'Pavel', 'Semenov', 45, 'm')

+ **INSERT INTO** *users* (ID, name, surname, age, gender) **VALUES** (3, 'Marina', 'Pavlova', 18, 'f')


## *Добавление колонки в таблицу:*
+ **ALTER TABLE** *users* **ADD** town varchar(40)


## *Обновление данных в таблицу:*
+ **UPDATE** *users*
  **SET** town = 'Saint.P' **WHERE** gender = 'm'

+ **UPDATE** *users*
  **SET** age = 27 **WHERE** name like 'P%'

+ **UPDATE** *users*
  **SET** name = 'Anton' **WHERE** id = 1

## *Удаление записи из таблицы:*
+ **DELETE** from *users* **WHERE** id = 2

+ **DELETE** from *users* **WHERE** age < 20

## *Удаление всех записей из таблицы:*
+ **TRUNCATE** *users*

## *Удаление таблицы:*
+ **DROP TABLE** *users*

# ***Работа с Java 1.8.0_351***

+ Скачал установочный файл с [сайта](https://www.filepuma.com/download/java_development_kit_64bit_8.0.3510.10-33896/download/)
+ Установил на пк скачанный файл
+ С помощью команды **Win+R** открыл командную строку
+ В командной строке ввел команду:
```
java -version
```
+ Получил результат:
```
java version "1.8.0_351"
Java(TM) SE Runtime Environment (build 1.8.0_351-b10)
Java HotSpot(TM) 64-Bit Server VM (build 25.351-b10, mixed mode)
```