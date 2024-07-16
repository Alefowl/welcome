# Отчет о работе с базой данных и установке Java 8

#### Дата составления: 15.09.2024
#### Составитель: Даниил Мартынов
_______________________________________________________________________________
## Работа с PostgresSQL
### 1. Создание базы данных
```sql
CREATE DATABASE test_db;
```
### 2. Создание таблицы
```sql
CREATE TABLE IF NOT EXISTS users (
	id SERIAL PRIMARY KEY,
	username VARCHAR(255) UNIQUE NOT NULL,
	email VARCHAR(255) UNIQUE NOT NULL,
	first_name VARCHAR(255) NOT NULL,
	second_name VARCHAR(255) NOT NULL,
	birthday DATE NOT NULL,
	status VARCHAR(255) NOT NULL
);
```
### 3. Внесение записей в базу данных
```sql
INSERT INTO users (username, email, first_name, second_name, birthday, status) 
VALUES 
('Ivan90', 'Ivan90@mail.ru', 'Ivan', 'Ivanov', '1990-07-15', 'trainee'),
('Sergey87', 'Sergey87@mail.ru', 'Sergey', 'Sergeev', '1987-12-09', 'trainee'),
('Alexey99', 'Alexey99@mail.ru', 'Alexey', 'Alexeev', '1999-10-03', 'trainee');
```
### 4. Изменение записей в базе данных
```sql
UPDATE users 
SET status = 'employee'
WHERE birthday > '1980-01-01';
```
### 5. Добавление колонки к таблице
```sql
ALTER TABLE users
ADD COLUMN gender VARCHAR(255);
```
### 5. Удаление записей из таблицы
```sql
DELETE FROM users
WHERE birthday > '1990-01-01';
```
### 6. Очистка таблицы
```sql
TRUNCATE TABLE users;
```
### 7. Удалите таблицу
```sql
DROP TABLE users;
```
## Установка Java 1.8.0_351
#### 1. Скачаем из [архива Oracle](https://www.oracle.com/java/technologies/javase/javase8u211-later-archive-downloads.html) файл jdk-8u351-macosx-x64.dmg
#### 2. Распаковываем и устанавливаем, следуя инструкции
#### 3. Вводим в терминал:
```cmd
java -version
```
#### 4. Получаем вывод:
```cmd
java version "1.8.0_351"
Java(TM) SE Runtime Environment (build 1.8.0_351-b10)
Java HotSpot(TM) 64-Bit Server VM (build 25.351-b10, mixed mode)
```