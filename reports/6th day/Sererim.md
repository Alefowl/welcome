Продукт: https://www.alefowl.com/ <br>
Дата проведения работ: 21.04.2024

***

## Работа с PostgresSQL


### 1. Создайте базу данных и таблицу в ней

Создание бд;

```sql
CREATE DATABASE test_db;
```

Для хранения данных потребуется enum:

```sql
CREATE TYPE sex AS ENUM ('M','F');
```

Создание таблицы:

```sql
CREATE TABLE IF NOT EXISTS test (
	id SERIAL PRIMARY KEY,
	firstname VARCHAR(25) NOT NULL,
	secondname VARCHAR(25) NOT NULL,
	surename VARCHAR(50) NOT NULL,
	age INT CHECK (age >= 0),
	date_of_birth DATE NOT NULL,
	gender sex
);
```

### 2. Внесите в базу данных 3 записи с помощью sql-запросов.

```sql
INSERT INTO test (firstname, secondname, surename, age, date_of_birth, gender) 
VALUES 
('William', 'Henry', 'Gaytes', 68, '1955-10-28', 'M'),
('Neall', 'Ellis', 'Ellis', 75, '1949-11-24', 'M'),
('Robert', 'Cecil', 'Martin', 71, '1952-12-05', 'M');
```

### 3. Измените 3 записи с помощью sql-запросов.
```sql
UPDATE test 
SET age = age + 1
WHERE id >= 0 AND id <= 3;
```

### 4. Добавьте 1 колонку к таблице с помощью sql-запросов.

Сделаем enum для хранения состояния человека:

```sql
CREATE TYPE life AS ENUM(
    'alive',
    'dead'
);
```

Добавим колонку:
```sql
ALTER TABLE test
ADD COLUMN status life NOT NULL DEFAULT 'alive';
```

### 5. Удалите 2 записи с помощью sql-запросов.

Добавим две записи:
```sql
INSERT INTO test 
(firstname, secondname, surename, age, date_of_birth, gender, status)
VALUES
('Nikola', ' Tesla', 'Tesla', 86, '1856-07-10', 'M', 'dead' ),
('René', 'Jean-Marie-Joseph', 'Guénon', 64, '1886-10-15', 'M', 'dead');
```

Теперь удалим их:
```sql
DELETE FROM test
WHERE status = 'dead';
```

### 6. Очистите всю таблицу с помощью sql-запросов.

```sql
DELETE FROM test;
```

Или

```sql
TRUNCATE TABLE test;
```


### 7. Удалите таблицу.

```sql
DROP TABLE test;
```

## Установка Java 1.8.0_351

Версия java [Java SE 8u351 b34](https://www.oracle.com/java/technologies/javase/8u351-relnotes.html)

Скачаем из [архива](https://www.oracle.com/java/technologies/javase/javase8u211-later-archive-downloads.html)

Вводим в терминал:
```cmd
java -version
```

Вывод:
```cmd
java version "1.8.0_351"
Java(TM) SE Runtime Environment (build 1.8.0_351-b10)
Java HotSpot(TM) 64-Bit Server VM (build 25.351-b10, mixed mode)
```
