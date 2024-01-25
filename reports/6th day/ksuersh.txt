Дата заполнения отчета 24.01.24 
Окружение: macOS: Ventura 13.0
Браузер: Safari Версия 16.1 (18614.2.9.1.12)

PostregeSQL:

Установлено приложение Postrege.app

Создана база данных под названием alefowl — CREATE DATABASE alefowl;

Создана таблица books — CREATE TABLE books (
id INT,
author TEXT,
metabook TEXT,
language TEXT,
year INT
);

Внесены в базу данных 3 записи — INSERT INTO books VALUES (1, ‘Chehov’, ‘Kashtanka’, ‘English’, 1887);
INSERT INTO books VALUES (2, ‘Chehov’, ‘Lady with the dog’, ‘English’, 1889);
INSERT INTO books VALUES (3, ‘Dostaevskii’, ‘Demons’, ‘English’, 1872);

Таблица проверена, путем получения содержимого — SELECT * FROM books; 

Изменены 3 записи — UPDATE books SET language=‘russian’ WHERE id=1;
UPDATE books SET language=‘russian’, year=1871 WHERE id=3; 

Добавлена 1 колонка — ALTER TABLE books ADD ready TEXT; 

Удалены 2 записи — DELETE FROM books WHERE id=1;
DELETE FROM books WHERE id=3;
 
Очищена вся таблица — DELETE FROM books; 

Удалена вся таблица — DROP TABLE books; 

Краткое описание установки JAVA 8 
С сайта Java.com выгружен файл jre-8u311-macosx-x64.dmg. 
В загрузках выбран данный файл и запущен, путем двойного щелчка по нему. 
В открывшемся диалоговом окне запущен мастер установки и нажата кнопка “Open”. 
На экране приветствия установки выбрана кнопка “install”
В диалоговом окне установщика MacJRE введен пароль и нажата кнопка «продолжить»
По завершении установки появился экран подтверждения. Далее нажата кнопка закрыть. 
Для проверки версии в терминале введена команда java -version. Выведено на экран: java version “1.8.0_401” 
