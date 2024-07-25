### Перечень SQL-запросов:

**create database** mathematics;

**create table** gradest_list (  
	id integer,  
	name varchar(10),  
	last_name varchar(10),  
	work varchar(10),  
	mark integer);  

**insert into** gradest_list **values** ('1', 'Ívan', 'Ivanov', 'homework', '5');  
**insert into** gradest_list **values** ('2', 'Petr', 'Petrov', 'classwork', '4');  
**insert into** gradest_list **values** ('3', 'Anna', 'Anina', 'test','3');  

**update** gradest_list **set** name = 'Oleg' **where** id = '1';  
**update** gradest_list **set** last_name = 'Sobolev' **where** name = 'Petr';  
**update** gradest_list **set** mark = '5' **where** name = 'Anna';

**alter table** gradest_list **add column** comment text;  

**delete from** gradest_list **where** name = 'Oleg';  
**delete from** gradest_list **where** mark = '4';

**truncate** gradest_list;

**drop table** gradest_list;

### Процесс установки Java 1.8.0_351:

1) Предварительно удалить имеющуюся на компьютере версию Java.  
2) Скачать файл-установщик Java_Runtime_Environment_(64 bit)_v8_Update_351.exe.  
3) Запустить программу-установщик, дождаться окончания установки.  
4) Проверить соответствие версии вводом в командную строку  
   > java -version.  
7) Получить ответ:  
   > java version "1.8.0_351".  
9) Готово, вы великолепны!  
    
