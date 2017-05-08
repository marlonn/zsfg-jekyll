---
layout: page
title: SQL
---

# **SQL-Syntaxelemente**

[Quelle: Codecademy]("https://www.codecademy.com/courses/learn-sql/lessons/multiple-tables/exercises/generalizations-multiple-tables?action=lesson_resume&link_content_target=interstitial_lesson")


### **General Information**
SQL is a programming language designed to manipulate and manage data stored in **relational databases**.  
A **relational database** is a database that organizes information into one or more **tables**.
A **table** is a collection of data organized into rows and columns.

A **statement** is a string of characters that the database recognizes as a valid command.

**CREATE TABLE** creates a new table.

**INSERT INTO** adds a new row to a table.

**SELECT** queries data from a table.

**UPDATE** edits a row in a table.

**ALTER TABLE** changes an existing table.

**DELETE FROM** deletes rows from a table.



**Primary Key** is a column that serves a unique identifier for row in the table. Values in this column must be unique and cannot be NULL.

**Foreign Key** is a column that contains the primary key to another table in the database. It is used to identify a particular row in the referenced table.
Joins are used in SQL to combine data from multiple tables.


### **Queries**

**SELECT** is the clause you use every time you want to query information from a database.

**WHERE** is a popular command that lets you filter the results of the query based on conditions that you specify.

**LIKE** and **BETWEEN** are special operators that can be used in a WHERE clause.

**AND** and **OR **are special operators that you can use with WHERE to filter the query on two or more conditions.

**ORDER BY** lets you sort the results of the query in either ascending or descending order.

**LIMIT** lets you specify the maximum number of rows that the query will return. This is especially important in large tables that have thousands or even millions of rows.


### **Joins**
**INNER JOIN** will combine rows from different tables if the join condition is true.  
Syntax:

    SELECT * FROM albums
    JOIN artists ON albums.artist_id = artists.id;

**LEFT OUTER JOIN** will return every row in the left table, and if the join condition is not met, NULL values are used to fill in the columns from the right table.  
Syntax:

    SELECT * FROM albums
    LEFT JOIN artists ON albums.artist_id = artists.id;

**CROSS JOIN** is not very useful. It combines every row of the first table with every row of the second table.  
Syntax:

    SELECT albums.name, albums.year, artists.name
    FROM albums, artists


### **As**
**AS** is a keyword in SQL that allows you to rename a column or table in the result set using an alias.  
Syntax:

    SELECT  albums.name AS 'Album',
            albums.year,
            artists.name AS 'Artist'
    FROM albums
    JOIN artists ON albums.artist_id = artists.id


### **Aggregate Functions**
**Aggregate functions** combine multiple rows together to form a single value of more meaningful information.

**COUNT** takes the name of a column(s) as an argument and counts the number of rows where the value(s) is not NULL.  
Syntax:

    SELECT COUNT(column_name) FROM table_name

**GROUP BY** is a clause used with aggregate functions to combine data from one or more columns.

**SUM()** takes the column name as an argument and returns the sum of all the values in that column.

**MAX()** takes the column name as an argument and returns the largest value in that column.

**MIN()** takes the column name as an argument and returns the smallest value in that column.

**AVG()** takes a column name as an argument and returns the average value for that column.
