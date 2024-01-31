# Отчет 31.01.2024

### Работа с СУБД PostgreSQL
**SQL-запросы**

*1. Создание таблицы:*

CREATE TABLE FOOD (

id INT PRIMARY KEY,

name TEXT,

price INTEGER,

spice TEXT,

weight TEXT

);

*2. Добавление в таблицу записей*

INSERT INTO FOOD (ID, name, price, spice, weight) VALUES (1, 'strips', '154', 'pepper', 'small');

INSERT INTO FOOD (ID, name, price, spice, weight) VALUES (2, 'fry', '189', 'salt', 'big');

INSERT INTO FOOD (ID, name, price, spice, weight) VALUES (3, 'chef burger de luxe', '189', 'sauce', 'medium');

*3. Проверка содержимого*

SELECT * FROM FOOD

*4. Изменение записей*

UPDATE FOOD set weight ='big' WHERE id = 1;

UPDATE FOOD SET price = 190 WHERE ID = 2;

UPDATE FOOD set name = 'burger' WHERE ID = 3;

*5. Добавление колонки*

ALTER TABLE FOOD ADD taste TEXT;

*6. Удаление записей*

DELETE FROM FOOD WHERE id=1;

DELETE FROM FOOD WHERE id=3;

*7. Очищение всей таблицы*

DELETE FROM FOOD;

*8. Удаление всей таблицы*

DROP TABLE FOOD;

### Работа с Java 8

1. Скачивание Java Development Kit (64bit)
2. Установка программы
3. Открытие командной строки с помощью Win + R, ввод "cmd"
4. Ввод команды "java -version"
5. Результат: 

java version "1.8.0_351"

Java(TM) SE Runtime Environment (build 1.8.0_351-b10)

Java HotSpot(TM) 64-Bit Server VM (build 25.351-b10, mixed mode)