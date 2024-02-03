# PostgreSQL
1. Создание БД  
```
create database AlefowlSample;
```
2. Создание таблицы  
```
create table people (
    id serial primary key,
    name varchar(70) not null,
    age int not null,
    height int not null,
    weight int not null,
    job varchar(120) not null,
    );
```
3. Заполнение БД  
```
insert into people (name, age, height, weight, job)
values
    ('Boris', 24, 178, 74, 'Developer'),
    ('Kate', 31, 163, 49, 'Product manager'),
    ('Ivan', 29, 190, 112, 'QA');
```
4. Изменение содержимого БД
```
update people
    set age = age + 1
    WHERE age > 18;
```
5. Добавление колонки в таблицу 
```
alter table people
    add email varchar(256);
```
6. Удаление записей в таблице
```
delete from people
    where age > 25;
```
7. Удаление всего содержимого таблицы
```
truncate people;
```
8. Удаление таблицы
```
drop table people;
```

# Установка и изменение версии JDK 
1. Скачал `jdk1.8.0_351` с сайта Oracle
2. Открыл файл `.zshrc` и добавил строки:
```
export JAVA_HOME=/Library/Java/JavaVirtualMachines/jdk1.8.0_351.jdk/Contents/Home
export PATH="/Library/Java/JavaVirtualMachines/jdk1.8.0_351.jdk/Contents/Home/bin:$PATH"%
```
3. Выполнил команду `source .zshrc`
4. Перезапустил терминал и проверил вирсию jdk командой `java -version`. Получил вывод:
```
java version "1.8.0_351"
Java(TM) SE Runtime Environment (build 1.8.0_351-b10)
Java HotSpot(TM) 64-Bit Server VM (build 25.351-b10, mixed mode)
```
