## Установка Java 1.8.0_351

1. Скачала и установила Java 8 
2. В терминале ввела команду java -version (_результат команды_): 

java version "1.8.0_351"

Java(TM) SE Runtime Environment (build 1.8.0_351-b10)

Java HotSpot(TM) 64-Bit Server VM (build 25.351-b10, mixed mode)

## Работа с СУБД PostgreSQL:

>**Создание БД:**

**CREATE DATABASE** TestStore;

>**Создание таблицы:**

**CREATE TABLE** Employees(
id int **PRIMARY KEY**,
age **VARCHAR**(2),
city **VARCHAR**(50),
name **VARCHAR**(30),
email **VARCHAR**(100)
);

>**Внесение записей в таблицу:**

**INSERT INTO** (id, age, city, name, email) **VALUES** (1, 23, 'Samara', 'Marta', 'zzaaxx78@gmail.com');

**INSERT INTO** (id, age, city, name, email) **VALUES** (2, 45, 'Murmansk', 'Yan', 'yannay@list.ru');

**INSERT INTO** (id, age, city, name, email) **VALUES** (3, 20, 'Saint-Petersburg', 'Elena', 'elena2003@gmail.com');

>**Изменение записей:**

**UPDATE** Employees
**SET** email = 'elElena@icloud.com' **WHERE** name = 'Elena';

**UPDATE** Employees
**SET** city = 'Moscow' **WHERE** id = 1;

**UPDATE** Employees
**SET** age = 46 **WHERE** name = 'Marta';

>**Добавление колонки к таблице:**

**ALTER TABLE** Employees **add** date_of_birth **date**;

>**Удаление записей:**

**DELETE FROM** Employees **WHERE** id = 2;
**DELETE FROM** Employees **WHERE** name = 'Elena';

>**Очистить таблицу:**

**TRUNCATE** Employees;

>**Удалить таблицу:**

**DROP TABLE** Employees;