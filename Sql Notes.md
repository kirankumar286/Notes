# SQL (Structured Query Language) 

### SELECT * FROM shows;
- "*" asterisk means all columns.
- FROM keyword followed by the table name. shows is the name of the table we are requesting data from.
- ";"  we end the statement with a semicolon.

### SELECT id, name, genre FROM shows;
-  SQL keywords like SELECT and FROM are not case-sensitive, but it's common to write them in uppercase to distinguish them from column names (id, name, genre) and table names (shows), which are written in lowercase.

### SELECT DISTINCT genre FROM shows;
- DISTINCT is used to return just the unique values in a column, so no duplicates.

### SELECT * FROM shows WHERE year > 2020;
- Here are all the SQL comparison operators that we can use in a condition:
- = equal to
- != not equal to <>
- ">" greater than
- < less than
- ">=" greater than or equal to
- <= less than or equal to

### SELECT * FROM shows WHERE name LIKE 'T%';
- The LIKE operator can be used to search for a pattern in a column. It’s used in the WHERE clause.
- The percentage sign % is a wildcard character that can be used with LIKE. You can use it to match characters to a pattern of your desired query.
- The % can be used in different ways:
- A% matches values that begin with letter 'A'.
- %z matches values that end with 'z'.
- _ is used one space after or befor a leter in single quotes.

### SELECT * FROM shows WHERE year BETWEEN 2020 AND 2025;
### SELECT * FROM shows WHERE name BETWEEN 'A' AND 'D';

### SELECT name, genre, stream, year FROM shows ORDER BY year DESC;
- DESC is the descending
- The ORDER BY statement sorts rows of data in ascending or descending order. By default, this command sorts the data in ascending order. 

Here’s a recap:

- SELECT selects data FROM a database.
- SELECT * selects all the columns.
- DISTINCT returns unique values in a column.
- WHERE filters results based on a condition.
- Comparison operators: =, !=, >, <, >=, <=.
- LIKE operator searches for a specific pattern.
- BETWEEN operator matches values in a range.
- ORDER BY sorts data (ascending/descending).
- SELECT brand, model, price, sold FROM cars WHERE brand IN ('Ford', 'Chevrolet', 'Ferrari') 	AND sold IS FALSE; 
Aggregate functions are used to perform calculations and return a single value.

The most common aggregate functions are:

- COUNT(): returns the number of rows.
- SELECT COUNT(*) FROM table_name;
- MAX(): returns the largest value in a column.
- SELECT title, artist, MAX(plays) FROM playlist;
- MIN(): returns the smallest value in a column.
- SELECT MIN(plays) FROM playlist;
- SUM(): returns the total sum in a column.
- SELECT SUM(plays) FROM playlist;
- AVG(): returns the average value in a column.
- SELECT AVG(plays) FROM playlist;
  
Aggregate functions are used a ton with something called a GROUP BY
- SELECT genre, COUNT(*) FROM playlist GROUP BY genre;

What are the average Metascores for each of the genres?
- SELECT genre , avg(metascore) from games group by genre order by metascore desc;

### Creating Tables
- CREATE TABLE companies (
  id INTEGER,
  name TEXT,
  headquarters TEXT,
  year INTEGER);

### Inserting values
- INSERT INTO companies (id, name, headquarters, year) VALUES (1, 'Twitter', 'San Francisco 🌁', 2006);
- INSERT INTO companies (id, name, headquarters, year) VALUES (2, 'Duolingo', 'Pittsburgh 🐝', 2011);
- INSERT INTO companies (id, name, headquarters, year) VALUES (3, 'BeReal', 'Paris 🇫🇷', 2020);
- INSERT INTO companies (id, name, headquarters, year) VALUES (4, 'Codedex', 'New York 🗽', 2022);

### Altering table by adding columns and updating the content
- ALTER TABLE companies ADD COLUMN about TEXT;
- UPDATE companies SET name = 'X' WHERE name = 'Twitter';

### Inner join also known as join
- SELECT title , year , book_id, author_id from books join authors ON books.author_id = authors.id;

### Left join
- SELECT title , year , book_id, author_id from books left join authors ON books.author_id = authors.id;

### UNION The UNION operator in SQL combines two tables into one list, without duplicates.
- SELECT columns FROM table1 UNION SELECT columns FROM table2;
