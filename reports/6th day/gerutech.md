# Отчет - день 6.

Установка и работа с PostgreSQL, установка Java
Дата: 02.07.2024

## PostgreSQL

1. Устанавливаем СУБД PostgreSQL открываем SQL Shell(psql).

2. Создаем БД с помощью SQL-запроса:

   ```SQL
   CREATE DATABASE firstdb;
   ```

3. Создаем таблицу с атрибутами с помощью SQL-запроса:

   ```SQL
   CREATE TABLE book(
   book_id integer NOT NULL PRIMARY KEY,
   isbn varchar(30) NOT NULL,
   title text NOT NULL,
   pub_year integer NOT NULL,
   author text NOT NULL,
   publisher varchar(50) NOT NULL
   );
   ```

   4. Вносим в БД записи с помощью SQL-запроса:

   ```SQL
   INSERT INTO book(
    book_id, title, isbn, pub_year, author, publisher
   )
   VALUES
   ('1',  'Язык как инстинкт', '978-5-00139-250-7', '2024','Пинкер Стивен', 'Альпина нон-фикшн'),
   ('2', 'Самурай без меча','9789851548534', '2024', 'Масао Китами','Поппури'),
   ('3', 'Лени Рифеншталь. Мемуары','9785862184624', '2011', 'Рифеншталь Лени', 'Ладомир');

   ```

4. Изменяем записи с помощью SQL-запроса:

   ```SQL
   UPDATE book SET author = 'Пинкер Стивен (Канада)'
   WHERE author = 'Пинкер Стивен';

   UPDATE book SET author = 'Рифеншталь Лени (Германия)'
   WHERE book_id = 3;

   UPDATE book SET author = 'Масао Китами (Япония)'
   WHERE title = 'Самурай без меча';

   ```

5. Добавляем колонку к таблице с помощью SQL-запроса:
   ```SQL
   ALTER TABLE book
   ADD COLUMN book_lang text DEFAULT('русский');
   ```
6. Удаляем записи с помощью sql-запроса:

   ```SQL
   DELETE FROM book
   WHERE book_id = 1;
   DELETE FROM book
   WHERE pub_year < 2020;
   ```

7. Очищаем таблицу с помощью sql-запроса:

   ```SQL
   DELETE FROM book;
   ```

8. Удаляем таблицу c помощью запроса:
   ```SQL
   DROP TABLE book;
   ```

## Java

1. Находим через поисковик и скачиваем файл *_Java_Runtime_Environment_(64bit)\_v8_Update_351.exe_* и выполняем установку.

2. Вводим локально в терминале команду:

   ```bash
   java -version
   ```

   выводится:

   ```
    java version "1.8.0_351"
    Java (TM) SE Runtime Environment (build 1.8.0_351-b10)
    Java HotSpot(TM) 64-Bit Server VM (build 25.351-b10, mixed mode)
   ```
