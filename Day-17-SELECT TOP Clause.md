# SELECT TOP Clause

SELECT TOP clause is used to fetch limited number of rows from a database. This clause is very useful while dealing with large databases.

**Syntax**
``` sh
SELECT TOP value column1,column2 FROM table_name;
``` 

value: number of rows to return from top

column1 , column2: fields in the table

table_name: name of table

**Syntax using Percent**
``` sh
SELECT TOP value PERCENT column1,column2 FROM table_name;
``` 

value: percentage of number of rows to return from top

column1 , column2: fields in the table

table_name: name of table

**To fetch first two data set from Student table**

``` sh
SELECT TOP 2 * FROM Student; 
``` 

**To fetch 50 percent of the total records from Student table.**

``` sh
SELECT TOP 50 PERCENT * FROM Student;
``` 

**For MySQL databases**
``` sh
SELECT column1,column2 FROM table_name LIMIT value;
``` 

column1 , column2: fields int the table

table_name: name of table

value: number of rows to return from top

**For Oracle databases**

``` sh
SELECT column1,column2 FROM table_name WHERE ROWNUM <= value;
``` 

column1 , column2: fields int the table

table_name: name of table

value: number of rows to return from top
