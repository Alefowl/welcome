Дата: 22.06.2024
ОС: Windows 11 Version 23H2 
SQL: PostgreSQL
Версия: 16

Создание таблицы:
CREATE TABLE Vehicles(
	id SERIAL PRIMARY KEY, 
	vehicle_name VARCHAR(30), 
	model VARCHAR(30), 
	issue_date DATE,
	vehicle_power INTEGER
);

Добавление данных в таблицу:
INSERT INTO public.vehicles(vehicle_name, model, issue_date, vehicle_power)
	VALUES ('audi', 'Q5','2004-10-19', 500), 
	('nissan', 'GTR', '2010-12-01', 900),
	('lada', 'granta','2000-09-14', 159);

Изменение данных:
UPDATE public.vehicles
	SET vehicle_power=1000
	WHERE public.vehicles.vehicle_name = 'audi';

UPDATE public.vehicles
	SET model='murano'
	WHERE public.vehicles.vehicle_name = 'nissan';

UPDATE public.vehicles
	SET vehicle_power=120
	WHERE public.vehicles.vehicle_name = 'lada';


Добавление столбца:
ALTER TABLE public.vehicles 
	ADD fuel_type VARCHAR(30);

Удаление данных:
DELETE FROM public.vehicles 
	WHERE id=1;

DELETE FROM public.vehicles 
	WHERE vehicle_power=900;

Удаление всех данных:
DELETE FROM public.vehicles

Удаление таблицы:
DROP TABLE public.vehicles



Установка Java 
Скачивание файла "jdk-8u351-windows-x64.exe"
Установка
Выполнение команды java -version
Ответ:
java version "1.8.0_351"
Java(TM) SE Runtime Environment (build 1.8.0_351-b10)
Java HotSpot(TM) 64-Bit Server VM (build 25.351-b10, mixed mode)
