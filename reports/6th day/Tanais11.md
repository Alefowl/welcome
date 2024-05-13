Тестировщик: Девятнина Вероника
Дата : 11.05.2024
Окружение: ОС - Windows 10 PRO, процессор - Intel(R) Celeron(R) N4500 @ 1.10GHz   1.11 GHz,
браузер - Яндекс

JAVA 8

-Скачала файл "JAVA_Development_Kit_(64bit)_v8_Update_351 (1).exe"
-Произвела установку
-Открыла командную строку через команду cmd в поиске Windows
-Ввела команду java -version
-Ответ совпал с требованием в задании

PostgreSQL

-CREATE DATABASE students;
-CREATE TABLE faculty(
    ID INT PRIMARY KEY, name VARCHAR (100) NOT NULL
surname VARCHAR(100)NOT NULL, age INT NOT NULL,
gender VARCHAR(1) NOT NULL
)
-INSERT INTO faculty VALUES
(1, Avdoshina Dariya, 20, "f"),
(2, Mishina Tatiana, 25, "f"),
(3, Igoshin Oleg, 21, "m" )
-ALTER TABLE faculty ADD group VARCHAR(15)
-UPDATE faculty SET group "history" WHERE id=1
-UPDATE faculty SET group "tourism" WHERE id=2
-UPDATE faculty SET group "arheology" WHERE id=3
-DELETE from faculty WHERE name="Dariya"
-DELETE from faculty WHERE age=25
-TRUNCATE faculty
-DROP TABLE faculty