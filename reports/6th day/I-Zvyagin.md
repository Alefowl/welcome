## Работа в PostgreSQL
1. Создание базы данных


       CREATE DATABASE mylibrary;

2. Создание таблицы с 5 атрибутами


       CREATE TABLE Books( book_id INT NOT NULL GENERATED ALWAYS AS IDENTITY PRIMARY KEY,  
       autor VARCHAR(50), title VARCHAR(100),
       year INTEGER, pages INTEGER );    

3. Внесение 3 записей в таблицу


       INSERT INTO books (autor, title, year, pages) VALUES ('Pushkin', 'The captains daughter', 1836, 384);
       INSERT INTO books (autor, title, year, pages) VALUES ('Karl Marx', 'Das Kapital', 1867, 2640);
       INSERT INTO books (autor, title, year, pages) VALUES ('Folk', 'Kolobok', null, 5);

4. Внесение 3 изменений


    UPDATE books SET autor = 'Pushkin A.S.' WHERE title = 'The captains daughter';
    UPDATE books SET pages = 2641 WHERE year = 1867;
    UPDATE books SET year = 1861 WHERE autor = 'Folk';


5. Добавление 1 колонки


    ALTER TABLE books ADD imprint VARCHAR(100);

6. Удаление 2 записей


    DELETE FROM books WHERE book_id = 1;
    DELETE FROM books WHERE autor = 'Folk';

7. Очистка таблицы


    TRUNCATE books;

8. Удаление таблицы


    DROP TABLE books;

## Установка Java 1.8.0_351
1. Скачал Java 1.8.0_351
2. По команде в терминале java -version


    java version "1.8.0_351"
    Java(TM) SE Runtime Environment (build 1.8.0_351-b10)