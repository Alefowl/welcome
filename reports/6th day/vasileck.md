CREATE TABLE book(
    book_id SERIAL PRIMARY KEY,
    title VARCHAR(50),
    author VARCHAR(30),
    price DECIMAL(8,2),
    amount INT
);    

INSERT INTO book(title, author, price, amount) 
VALUES
	('Мастер и Маргарита', 'Булгаков М.А.', 670.99, 3),
	('Белая гвардия', 'Булгаков М.А.', 540.50, 5),
	('Братья Карамазовы', 'Достоевский Ф.М.', 799.01, 2);

UPDATE book
SET title = 'Идиот', author = 'Достоевский Ф.М.'
WHERE title = 'Белая гвардия'

UPDATE book
SET price = price * 0.5
WHERE author = 'Булгаков М.А.'

UPDATE book
SET amount = amount - 1
WHERE title = 'Братья Карамазовы'

ALTER TABLE book ADD COLUMN buy INT

DELETE FROM book WHERE title = 'Братья Карамазовы'

DELETE FROM book WHERE author = 'Булгаков М.А.'

TRUNCATE book

DROP TABLE book


Скачивание версии Java 1.8.0_351. Установка этой версии. Проверка версии в консоли с помощью команды  java -version. Вывод в консоли java version "1.8.0_351".