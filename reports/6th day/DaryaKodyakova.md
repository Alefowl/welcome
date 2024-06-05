Тестировщик: Кодякова Дарья
Дата составления отчета: 05.06.2024

### УСТАНОВКА PostgreSQL
- с сайта https://www.postgresql.org/ скачана и установлена PostgreSQL.
- с сайта https://www.postgresql.org/ скачана и установлена pgAdmin.

#### Создание базы данных и работа с таблицей:

##### _Создание таблицы:_
CREATE TABLE customers(
ID INT PRIMARY KEY,
name VARCHAR(100) NOT NULL,
surname VARCHAR(100) NOT NULL,
email VARCHAR(100) NOT NULL,
gender VARCHAR(3) NOT NULL

##### _Внесение данных:_
INSERT INTO customers
VALUES
(1, 'Иван', 'Иванов', 'ivanov@mail.ru', 'муж'),
(2, 'Анна', 'Анютина', 'anna.ant@mail.ru', 'жен'),
(3, 'Антон', 'Антонов', 'antonov@mail.ru', 'муж')

##### _Изменение данных:_
UPDATE customers
SET email = 'iv.ivan@mail.ru'
WHERE id = 1

UPDATE customers
SET name = 'Анастасия'
WHERE id = 2

UPDATE customers
SET surname = 'Ансонов'
WHERE id = 3

##### _Добавление колонки:_
ALTER TABLE customers ADD age INT

##### _Удаление записей:_
DELETE from customers WHERE gender = 'жен';
DELETE from customers WHERE name = 'Антон'

##### _Очищение таблицы:_
TRUNCATE customers

##### _Удаление таблицы:_
DROP TABLE customers


### УСТАНОВКА Java 1.8.0_351
- Скачана версия Java 1.8.0_351
- Выполнена установка.
- В переменных средах:
  -в файл Path добавлена ссылка на Java 1.8.0_351\bin;
  -создан файл JAVA_HOME, содержащий ссылку на Java 1.8.0_351

По запросу java -version в командной строке получен результат:
```sh
java version "1.8.0_351"
Java(TM) SE Runtime Environment (build 1.8.0_351-b10)
Java HotSpot(TM) 64-Bit Server VM (build 25.351-b10, mixed mode)
```