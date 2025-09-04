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
