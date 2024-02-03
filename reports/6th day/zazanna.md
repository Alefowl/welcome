# 03.02.2024

ОС Windows 10 Pro, версия 20H2 браузер Chrome версия 120.0.6099.217

### Создание БД и таблицы 
PostgreSQL 16 версия

DBeaver Версия 23.3.3.202401211839

<details><summary>SQL-запросы</summary>

1. **Создание БД**
create database persons;

2. **Создание таблицы**
  
create table Persons (

PersonID int,

LastName varchar(255),

FirstName varchar(255),

Address varchar(255),
City varchar(255)
);
3. **Внесение данных**

   insert into Persons (PersonID,LastName,FirstName,Address,City)
values (1,'Ivan','Bobrov','Nevskij 71','SPb')

   insert into Persons (PersonID,LastName,FirstName,Address,City)
values (2,'Alex','Belov','Nevskij 73','SPb')

   insert into Persons (PersonID,LastName,FirstName,Address,City)
   values (3,'Maria','Sokolova','Nevskij 75','SPb')
4. **Изменение данных**

 update PERSONS set firstname='Brain',City='moscow'where PERSONID=1;
 update PERSONS set firstname='Mikel',City='Gdov'where PERSONID=2;
 update PERSONS set lastname='Ivanova',City='Rostov'where PERSONID=3;
5. **Добавить 1 колонку**

alter table persons
add contry Text; 
6. **Удалить две записи** 

delete from persons where personID=1;

delete from persons where City='SPb';
7. **очистить таблицу**

TRUNCATE persons;
8. **Удалить таблицу**

DROP TABLE persons;

</details>

### Установите Java 1.8.0_351.

1. Скачать https://javadl.oracle.com/webapps/download/AutoDL?BundleId=247136_10e8cce67c7843478f41411b7003171c
2. Мастер установки
3. Открыть командную строку windows
4. ввести cmd
5. ввод команды "java -version"

результат соответсвтует требованиям

Java(TM) SE Runtime Environment (build 1.8.0_351-b10)

Java HotSpot(TM) 64-Bit Server VM (build 25.351-b10, mixed mode)
