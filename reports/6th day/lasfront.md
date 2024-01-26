# Отчет 24.01.2024

### Работа с СУБД PostgreSQL

**Окружение**:

PostgreSQL 16.1, 64-bit.

Работа с БД проведена в двух вариантах с использованием:

1. DBeaver Версия 23.3.3.202401211839.
2. SQL Shell (psql).

<details><summary>SQL-запросы</summary>

1. **Создание БД**.
   
create database alefowl_test;

2. **Создание таблицы**.

create table clients (

id int primary key,

name varchar(50),

city varchar(50),

email varchar(100),

category varchar(50),

total_orders int,

total_amount decimal(8,2));

3. **Заполнение таблицы**.

insert into clients (id, name, city, email, category, total_orders, total_amount) values (1, 'Борзов Иван', 'Ставрополь', 'qwer@mail.ru', 'новый клиент', 12, 2590.25);

insert into clients (id, name, city, email, category, total_orders, total_amount) values (2, 'Калинина Анна', 'Иваново', 'asdfg@mail.ru', 'постоянный клиент', 207, 29500.15);

insert into clients (id, name, city, email, category, total_orders, total_amount) values (3, 'Котов Николай', 'Москва', 'zxvcn12ggh@gmail.com', 'неактивный', 3, 1458.12);

insert into clients (id, name, city, email, category, total_orders, total_amount) values (4, 'Котова Елена', 'Москва', 'fgtyhn@gmail.com', 'неактивный', 0, 0.00);

4. **Добавление колонки в таблицу**.

alter table clients
add date_last_order date;

5. **Изменение записей в таблице**.

update clients
set email = 'borzov123@gmail.ru'
where id = 1;

update clients
set category = 'постоянный клиент'
where total_orders > 10;

update clients
set category = 'новый клиент'
where total_orders between 1 and 9 and total_amount > 1000.00;

update clients
set date_last_order = '2023-10-25'
where id = 1;

update clients
set date_last_order = '2024-01-05'
where id = 2;

update clients
set date_last_order = '2022-11-25'
where id = 3;

6. **Удаление записей из таблицы**.

delete from clients
where category = 'неактивный' or total_orders < 1;

delete from clients
where (extract(year from age(current_date, date_last_order)) * 12 + extract(month from age(current_date, date_last_order))) > 12;

7. **Очистка таблицы**.

truncate clients;

8. **Удаление таблицы**.

drop table clients;

</details>

### Установка Java

Oкружение: OC: Windows 10 Версия 22H2 64 bit.

Проведено обновление версии Java 11 на Java 8.

<details><summary>Шаги</summary>

1. Скачать Java Development Kit (64bit) /[скачивала по ссылке](https://www.filepuma.com/download/java_development_kit_64bit_8.0.3510.10-33896/)/

2. Найти в Панеле управления "Изменение системных переменных среды".

3. В "Переменные среды" / "Системные переменные" в строке JAVA HOME указать путь к скаченному файлу `C:\Program Files\Java\jdk1.8.0_351`.

4. Там же в path указать путь до папки bin `C:\Program Files\Java\jdk1.8.0_351\bin`.

5. Проверить версию Java в командной строке. 

</details>

**Проверка версии Java после обновления**.

Команда: 

`java -version`

Результат: 

`java version "1.8.0_351"`

`Java(TM) SE Runtime Environment (build 1.8.0_351-b10)`

`Java HotSpot(TM) 64-Bit Server VM (build 25.351-b10, mixed mode)`
