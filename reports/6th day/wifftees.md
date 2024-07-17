# Взаимодействие с таблицами PostgreSQL
## Установка
1. `sudo apt install postgresql postgresql-contrib`
2. Запуск: `sudo systemctl start postgresql.service`
3. Заходим под дефолтного пользователя: `sudo -i -u postgres`
4. Запускаем консоль: `psql`
##
1. Создание базы `CREATE DATABASE wifftees;`
2. Создание таблицы: 
    ```
    CREATE TABLE _car(
      id SERIAL PRIMARY KEY,
      model VARCHAR(255) NOT NULL,
      producer VARCHAR(255) NOT NULL,
      color VARCHAR(255) NOT NULL,
      price DECIMAL(10, 2) NOT NULL,
      year INTEGER NOT NULL
    );
    ```
3. Добавление элементов таблицы
    ```
    INSERT INTO _car (model, producer, color, price, year) 
    VALUES 
      ('Model S', 'Tesla', 'Red', 79999.99, 2021),
      ('Mustang', 'Ford', 'Blue', 55999.99, 2020),
      ('Civic', 'Honda', 'Black', 22999.99, 2019);
    ```
4. Обновление элементов таблицы
    ```
    UPDATE _car SET color = 'black' WHERE price > 20000.00;
    ```
5. Добавление атрибута
    ```
    ALTER TABLE _car
    ADD COLUMN mileage INTEGER;
    ```
6. Удаление элементов таблицы
    ```
    DELETE FROM _car WHERE model = 'Civic' OR model = 'Mustang';
    ```
7. Очистка таблицы
    ```
    TRUNCATE TABLE _car;
    ```
8. Удаление таблицы
    ```
    DROP TABLE _car;
    ```
# Установка Java версии 1.8.0_351
1. С помощью команды `uname -m` посмотрим текущую архитектуру
2. Зайдем в [архив](https://www.oracle.com/java/technologies/javase/javase8u211-later-archive-downloads.html) и выберем версию, которая соответствует архитектуре и OC 
3. С помощью командной строки создадим директорию, в которой будут лежать бинарники нужной версии: `sudo mkdir /opt/jdk`
4. После того, как мы скачали архив нужной версии (он будет лежать в  `~/Downloads/`), распакуем его в нужную директорию:
    ```
    sudo tar -zxf ~/Downloads/jdk-8u351-linux-i586.tar.gz -C /opt/jdk
    ```
5. Бинарные файлы необходимой версии можно использовать `/opt/jdk/jdk1.8.0_351/bin/java -version`
6. Чтобы сделать файлы 8-й java бинарными файлами по умолчанию необходимо выполнить:
    ```
    sudo update-alternatives --install /usr/bin/java java /opt/jdk/jdk1.8.0_351/bin/java 1
    ```



