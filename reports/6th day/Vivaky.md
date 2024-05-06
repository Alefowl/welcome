# **Работа с Java 1.8.0_351**
+ скачал с [сайта](https://www.filepuma.com/download/java_development_kit_64bit_8.0.3510.10-33896/download/)
+ установил
+ проверил версию в командной строке
#
# **Работа с SQL**
+ CREATE DATABASE test
+ CREATE TABLE people(                                
       ID INT PRIMARY KEY,                                 
       name VARCHAR(100) NOT NULL,                                        
       surname VARCHAR(100) NOT NULL,                          
       age INT NOT NULL,                               
       gender VARCHAR(1) NOT NULL                     
  )                                   
+ INSERT INTO people                                          
VALUES                                        
(1, 'Ulyana', 'Ulyashovna', 40, 'ж'),                          
(2, 'Dgokalina', 'Simple', 5, 'ж'),                         
(3, 'Sharik', 'Sobakovich', 80, 'м')
+ ALTER TABLE people ADD country varchar(40)
+ UPDATE people                            
SET country = 'USA'                         
WHERE gender = 'ж'
+ UPDATE people                                 
SET country = 'Zimbaba'                     
WHERE age > 60
+ UPDATE people                             
SET name = 'Book'                                  
WHERE id = 3
+ DELETE from people WHERE age = 5;                                                                         
DELETE from people WHERE name = 'Book'
+ TRUNCATE people
+ DROP TABLE people
