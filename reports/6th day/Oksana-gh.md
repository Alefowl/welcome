День стажировки: 6.  
Дата отчета: 20.02.2024


## 1. СУБД PostgreSQL  
_PostgreSQL версия 16.2_

Создание БД:  
>CREATE DATABASE books;

Создание таблицы:  
>CREATE TABLE Mybook (id INT, title TEXT, author TEXT, language TEXT, year INT);

Внесение данных:  
>INSERT INTO Mybook (id, title, author, language, year) VALUES (1, 'Time Regained', 'Marcel Proust', 'English', 1931);  
INSERT INTO Mybook (id, title, author, language, year) VALUES (2, 'Pères et Enfants', 'Ivan Turgenev', 'French', 1863);  
INSERT INTO Mybook (id, title, author, language, year) VALUES (3, 'The Queen of Spades', 'Alexander Pushkin', 'English', 1834);  

Изменение данных:  
>UPDATE Mybook SET title = ‘Time’ WHERE id=1;   
UPDATE Mybook SET author = ‘Turgenev’ WHERE id=3;  
UPDATE Mybook SET year = 2024 WHERE id=2;  

Добавление колонки:  
>ALTER TABLE Mybook ADD metabook TEXT;

Удаление записей:  
>DELETE FROM Mybook WHERE id=2;   
DELETE FROM Mybook WHERE id=3;

Очищение таблицы:  
>DELETE FROM Mybook;

Удаление таблицы:  
>DROP TABLE Mybook;



## 2. JAVA 8

* Скачивание файла "Java_Development_Kit_(64bit)_v8_Update_351 (1).exe".
* Установка.
* Открытие командной строки (cmd в поиске Windows).
* Выполнение команды java -version.
* Ответ:
>java version "1.8.0_351"  
Java(TM) SE Runtime Environment (build 1.8.0_351-b10)  
Java HotSpot(TM) 64-Bit Server VM (build 25.351-b10, mixed mode)
