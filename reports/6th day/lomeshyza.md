**дата: 12.02.2024**

## Установка Java 1.8.0_351

1. Удаление старых версий Java.
2. Установка новой версии виртуальной машины по инструкции установщика.
3. Введение команды java -version.
4. Получение ответа: 
java version "1.8.0_351"
Java(TM) SE Runtime Environment (build 1.8.0_351-b10)
Java HotSpot(TM) 64-Bit Server VM (build 25.351-b10, mixed mode)

## Работа с СУБД PostgreSQL. 

**1. Cоздайте базу данных и таблицу:**

``
CREATE DATABASE test;
``

``
CREATE TABLE idiot (
id INT PRIMARY KEY,
name_rus VARCHAR,
name_fr VARCHAR,
age INT,
gender CHAR
);
``

**2. Внести в базу данных 3 записи:**

insert into idiot 
values (1, 'Мышкин', 'Le prince', 26, 'm');

insert into idiot 
values (2, 'Настасья Филипповна', 'Nastasie Philippovna', 25, 'f');

insert into idiot 
values (3, 'Парфен Рогожин', 'Parfione Rogojine', 27, 'm');


**3. Изменить 3 записи:**

update idiot set name_rus = 'Настасья' 
where id=2;

update idiot set name_rus = 'Рогожин', name_fr = 'Rogojine' 
where id=3;


**4. Добавить 1 колонку к таблице:**

alter table idiot add city char;

**5. Удалить 2 записи:**

DELETE FROM idiot WHERE id=1;
DELETE FROM idiot WHERE id=2;

**6. Очистить всю таблицу:**

DELETE FROM idiot;

**7. Удалить таблицу:**

drop table idiot;




