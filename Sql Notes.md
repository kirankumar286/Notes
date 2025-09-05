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
