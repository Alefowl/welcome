# SQL-запросы

1. Создание базы данных:
   create database test;

2. Создание таблицы:
   create table users (
   id serial primary key,
   first_name VARCHAR(255) not null,
   middle_name VARCHAR(255) not null,
   last_name VARCHAR(255) not null,
   age INT not null,
   city VARCHAR(255) not null
   );

3. Добавление записей:
   insert into public.users (first_name, middle_name, last_name, age, city) values
   ('Ivan', 'Ivanovich', 'Ivanonv', 34, 'Moscow'),
   ('Alexey', 'Alexeyevich', 'Alexeev', 40, 'Ekaterinburg'),
   ('Maxim', 'Maximovich', 'Maximov', 52, 'Chelyabinsk');

4. Обновление записей:
   update public.users set city = 'Volgograd' where city = 'Moscow';
   update public.users set city = 'Kaliningrad' where city = 'Chelyabinsk';
   update public.users set city = 'Belgorod' where city = 'Ekaterinburg';

5. Изменение таблицы:
   alter table public.users
   add column hobby VARCHAR(255);

6. Удаление записей:
   delete from public.users where id = 1;
   delete from public.users where id = 2;

7. Очищение таблицы:
   truncate public.users;

8. Удаление таблицы:
   drop table public.users;

# Java 1.8.0_351

1. Скачать JRE - Java 1.8.0_351 с сайта https://www.filepuma.com/download/java_runtime_environment_64bit_8.0.3510.10-33899/.
2. Установить JRE.
3. Изменить текущую JRE на скаченную, изменить переменные в системных переменных.
4. Ввести в командную строку java -version и получить результат:<br>
   java version "1.8.0_351"
   Java(TM) SE Runtime Environment (build 1.8.0_351-b10)
   Java HotSpot(TM) 64-Bit Server VM (build 25.351-b10, mixed mode)