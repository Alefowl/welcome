Продукт: https://www.alefowl.com/
Дата проведения работ: 06.04.2024
Окружение: ОС – macOS Sonoma 14.0, процессор 3,3 GHz 6‑ядерный процессор Intel Core i5, браузер – Safari

Отчет:
Задание 1.

1)	Установлена СУБД PostgreSQL и iTerm-2 для работы с ней.
2)	С помощью цепочки команд 
psql
CREATE DATABASE test;
Создана база данных test
3)	\l проверено наличие базы данных
4)	\c test  подключена база данных test
5)	Создана таблица 
CREATE TABLESPACE my_first_table (
	name TEXT,
	surname TEXT,
	age INT,
	level_of_English TEXT,
	interests TEXT);
6)	Вставлены данные
INSERT INTO my_first_table (name, surname, age) VALUES ('Anna', 'Sinitsyna', INT'45');
INSERT INTO my_first_table (name, surname, age) VALUES ('Sarah', 'Bloom', INT'35');
INSERT INTO my_first_table (name, surname, age) VALUES ('Kitty', 'Sark', INT'25');
7)	Изменены данные
UPDATE my_first_table SET age=40 WHERE age=45;
UPDATE my_first_table SET surname = 'Orlova' WHERE surname = 'Sinitsyna';

8)	Добавлена колонка
ALTER TABLE my_first_table
ADD gender text;

9)	Удалены 2 записи
DELETE FROM my_first_table WHERE name = ‘Anna’;
DELETE FROM my_first_table WHERE name = ‘Liza’;

10)	Удалены все записи
DELETE FROM my_first_table;
11)	Удалена таблица
12)	DROP TABLE my_first_table;

Задание 2. 
Скачан образ диска для установки Java 1.8.0_351.
Выполнены шаги установки.
Установка проверена в Terminal.
