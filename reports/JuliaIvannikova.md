Тестировщик: Юлия Иванникова

Дата установки ПО: 12.04.2024
Окружение: ОС -  Windows 11 Pro, версия 23H2, сборка 22631.3296
Браузер - Google Chrome Версия 123.0.6312.105 (Официальная сборка), (64 бит)

Создание базы данных и таблицы с помощью SQL-запросов

PostgreSQL: версия 15.2
pgAdmin 4: версия 6.19

1. Создание БД

CREATE DATABASE Store;
 
2. Добавление таблицы в БД 

CREATE TABLE customers (
  id SERIAL PRIMARY KEY, 
  firstname character varying(200) NOT NULL, 
  lastname character varying(200) NOT NULL,
  phone character varying(30) NOT NULL, 
  email character varying(200) NOT NULL,
  address character varying(200) NOT NULL 
);

3. Внесение данных в таблицу

INSERT INTO customers (firstname, lastname, phone, email, address ) VALUES ( 'Сергей', 'Михайлов', '89992332244', 'michailov.serg@mail.ru','Москва' );
INSERT INTO customers (firstname, lastname, phone, email, address) VALUES ( 'Роман', 'Симонов', '89992334444', 'roma_simonov@mail.ru', 'Санкт-Петербург');
INSERT INTO customers (firstname, lastname, phone, email, address) VALUES ( 'Мария', 'Васильева', '89992334678', 'masha_111@mail.ru', 'Волгоград');

4. Изменение данных в таблице 

UPDATE customers SET firstname = 'Алексей' WHERE id = 1;
UPDATE customers SET phone = '89992335555' WHERE lastname = 'Симонов';
UPDATE customers SET address = 'Вологда' WHERE email = 'masha_111@mail.ru';

5. Добавление колонки к таблице 

ALTER TABLE customers ADD age character varying(10) NULL;

6. Удаление записей из таблицы

DELETE FROM customers WHERE address != 'Санкт-Петербург';

7. Очищение таблицы

TRUNCATE TABLE customers;

8. Удаление таблицы

DROP TABLE customers;


Установка Java 1.8.0_351

1. Скачан установочный файл “Java_Development_Kit_(64bit)_v8_Update_351.exe”
2. Пройдены шаги по установке Java 8.
3. В командной строке введено: 

java -version

Получен результат:

java version "1.8.0_351"
Java(TM) SE Runtime Environment (build 1.8.0_351-b10)
Java HotSpot(TM) 64-Bit Server VM (build 25.351-b10, mixed mode)

