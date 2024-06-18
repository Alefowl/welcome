### Продукт: https://www.alefowl.com/
### Дата проведения работ: 18.06.2024
### Система: Windows 10 Домашняя
### День стажировки: 6

#  Задача 1. Установка JDK, JAVA 8:
+ 1.1. Скачал файл по ссылке https://www.filepuma.com/download/java_development_kit_64bit_8.0.3510.10-33896/
 "Java_Development_Kit_(64bit)_v8_Update_351.exe"
+ 1.2. Произвел установку
+ 1.3. Открыл командную строку через "cmd" в Windows
+ 1.4. Ввел команду "java -version". Получен ответ:
 
 java version "1.8.0_351"

 Java(TM) SE runtime Environment(build 1.8.0_351-b10)

 Java HotSpot(TM) 64-Bit Server VM (build 25.351-b10, mixed mode) 

#  Задача 2. Установка СУБД и работа с запросами:
Установлена PostgreSQL 16.3-2, 64-bit, для работы с БД использована pgAdmin4

### 2.1. Создаем базу данных:
+ CREATE DATABASE geo_db

### 2.2. С помощью "Query Tool" cоздаем таблицу с 5-ю атрибутами:
+ CREATE TABLE cities(
id INTEGER,
title VARCHAR(50),
population INTEGER,
climat VARCHAR(50),
parts INTEGER
);

### 2.3. Вносим 3 записи:
+ INSERT INTO cities VALUES (1,'Toronto',50000,'Tropical',1),
+ INSERT INTO cities VALUES (2,'Monreal',70000,'Arctic',3),
+ INSERT INTO cities VALUES (3,'Edmonton',80000,'Continental',5)

### 2.4. Вносим изменения в 3 записи:
+ UPDATE cities SET title='Quebec' WHERE id=3;
+ UPDATE cities SET population=90000 WHERE parts=5;
+ UPDATE cities SET climat='Arctic' WHERE id=1

### 2.5. Добавляем 1 колонку к таблице:
+ ALTER TABLE cities ADD COLUMN extra INTEGER

### 2.6. Удаляем 2 записи:
+ DELETE FROM cities WHERE id=1;
+ DELETE FROM cities WHERE title='Quebec'

### 2.7. Очищаем таблицу:
+ DELETE FROM books; 

### 2.8. Удаляем таблицу
+ DROP TABLE cities; 