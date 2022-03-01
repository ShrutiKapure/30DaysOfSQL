# SQL UNION Operator

The UNION operator is used to combine the result-set of two or more SELECT statements.

•	Every SELECT statement within UNION must have the same number of columns

•	The columns must also have similar data types

•	The columns in every SELECT statement must also be in the same order

UNION Syntax

``` sh
SELECT column_name(s) FROM table1
UNION
SELECT column_name(s) FROM table2;
``` 

UNION ALL Syntax

The UNION operator selects only distinct values by default. To allow duplicate values, use UNION ALL:

``` sh
SELECT column_name(s) FROM table1
UNION ALL
SELECT column_name(s) FROM table2;
``` 

*Note: The column names in the result-set are usually equal to the column names in the first SELECT statement.*

Eg: The following SQL statement returns the cities (only distinct values) from both the "Students" and the "Teachers" table:

``` sh
SELECT City FROM Students 
UNION
SELECT City FROM Teachers 
ORDER BY City;
``` 

*Note: If some customers or suppliers have the same city, each city will only be listed once, because UNION selects only distinct values. 
Use UNION ALL to also select duplicate values!*

SQL UNION ALL Example

Eg: The following SQL statement returns the cities (duplicate values also) from both the "Students" and the "Teachers" table:

``` sh
SELECT City FROM Students 
UNION ALL
SELECT City FROM Teachers
ORDER BY City;
``` 
