     -Работа с СУБД PostgreSQL:

     1. Создание базы данных:
     
     CREATE DATABASE CT;

     2. Создание таблицы:
 
     CREATE TABLE cities (
     ID BIGSERIAL,
     Moscow VARCHAR(20),
     Paris VARCHAR(20),
     Tokyo VARCHAR(20),
     Berlin VARCHAR(20)
     );
   
    3. Добавление данных:

    Insert into cities (Moscow, Paris, Tokyo, Berlin) values (1, 3, 4, 64);
    Insert into cities values (Moscow, Paris, Tokyo, Berlin) (1, 3, 4, 64);
    Insert into cities values (Moscow, Paris, Tokyo, Berlin) (1, 3, 4, 64);

    4. Добавление строки:

    ALTER TABLE cities
    ADD London VARCHAR(20);

    5. Изменение данных: 
    
    UPDATE cities SET Moscow = 4;
    UPDATE cities SET Moscow = no;
    UPDATE cities SET Moscow = yes;

    6. Удаление записей:
   
    DELETE FROM cities WHERE Moscow = yes;
    DELETE FROM cities WHERE Paris = 3;

    7. Удаление таблицы:

    DROP TABLE cities;


    Установка Java 1.8.0_351:
    
    1) Удаление старой версии Java
    2) Поиск нужной версии
    3) Установка нужной версии
    4) Проверка версии через командную строку


