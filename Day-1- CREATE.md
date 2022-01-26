# SQL-CREATE Query

-**CREATE DATABASE**

The CREATE DATABASE statement is used to create a new SQL database.

**Syntax:**
` CREATE DATABASE database name; `

eg: `CREATE DATABASE shrutiDb;`

-**CREATE TABLE**

The CREATE TABLE statement is used to create a new table in a database.

**Syntax:**
``` sh
CREATE TABLE table_name
(
column1 data_type(size),
column2 data_type(size),
column3 data_type(size),
....
);
``` 
table_name: name of the table.
column1: name of the first column.
data_type: Type of data we want to store in the particular column. 
            For example,int for integer data.
size: Size of the data we can store in a particular column.

eg:
``` sh
CREATE TABLE Students
(
Name varchar(20),
Roll_No int(3),
Subject varchar(20),
);
``` 
