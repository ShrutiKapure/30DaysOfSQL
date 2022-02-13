# ORDER BY

The ORDER BY keyword is used to sort the result-set in ascending or descending order. 
The ORDER BY keyword sorts the records in ascending order by default. To sort the records in descending order, use the DESC keyword.
  
Syntax:

``` sh
SELECT column1, column2, ...
FROM table_name
ORDER BY column1, column2, ... ASC|DESC;
``` 

Eg:

``` sh
SELECT * FROM Students
ORDER BY Name;
DESCENDING ORDER
SELECT * FROM Students
ORDER BY roll_no DESC;
The following SQL statement selects all customers from the "Students" table, sorted by the "Country" and the "Name" column. 
/*This means that it orders by Country, but if some rows have the same Country, it orders them by Name:*/
  ``` 
``` sh  
SELECT * FROM Students
ORDER BY Country, Name;
/*The following SQL statement selects all customers from the "Students" table, sorted ascending by the "Country" and descending by the "Name" column:*/
``` 

``` sh
SELECT * FROM Students
ORDER BY Country ASC, Name DESC;
``` 

-**Sorting by column number**

Sort a database table accrding to column 1 i.e Roll_no

``` sh
CREATE TABLE studentinfo
( Roll_no INT,
NAME VARCHAR(30),
Address VARCHAR(30),
CONTACTNO BIGINT NOT NULL,
Age INT ); 
INSERT INTO studentinfo
VALUES (7,'ROHIT','GAZIABAD',9193458625,18),
(4,'DEEP','RAMNAGAR',9193458546,18),
(1,'HARSH','DELHI',9193342625,18),
(8,'NIRAJ','ALIPUR',9193678625,19),
(5,'SAPTARHI','KOLKATA',9193789625,19),
(2,'PRATIK','BIHAR',9193457825,19),
(6,'DHANRAJ','BARABAJAR',9193358625,20),
(3,'RIYANKA','SILIGURI',9193218625,20);
SELECT Name, Address
FROM studentinfo
ORDER BY 1
``` 


# GROUP BY

The GROUP BY Statement in SQL is used to arrange identical data into groups i.e if a particular column has same values
in different rows then it will arrange these rows in a group. 
   
GROUP BY clause is used with the SELECT statement.
  
In the query, GROUP BY clause is placed after the WHERE clause.
  
In the query, GROUP BY clause is placed before ORDER BY clause if used any.

Syntax:

``` sh
SELECT column1, function_name(column2)
FROM table_name
WHERE condition
GROUP BY column1, column2
ORDER BY column1, column2;
``` 

function_name: Name of the function used for example, SUM() , AVG().
  
table_name: Name of the table.
  
condition: Condition used.

Eg:

``` sh
SELECT COUNT(CustomerID), Country
FROM Customers
GROUP BY Country;
SELECT COUNT(CustomerID), Country
FROM Customers
GROUP BY Country
ORDER BY COUNT(CustomerID) DESC;
``` 

-**Group By single column**

Group By single column means, to place all the rows with same value of only that particular column in one group. 

  Consider the query as shown below:

``` sh
SELECT NAME, SUM(SALARY) FROM Employee 
GROUP BY NAME;
``` 

-**Group By multiple columns**

Group by multiple column is say for example, GROUP BY column1, column2.
  
This means to place all the rows with same values of both the columns column1 and column2 in one group. Consider the below query:

``` sh
SELECT SUBJECT, YEAR, Count(*)
FROM Student
GROUP BY SUBJECT, YEAR;
``` 

-**HAVING Clause**

The HAVING clause was added to SQL because the WHERE keyword cannot be used with aggregate functions.
  
Syntax:

``` sh
SELECT column1, function_name(column2)
FROM table_name
WHERE condition
GROUP BY column1, column2
HAVING condition
ORDER BY column1, column2;
``` 

function_name: Name of the function used for example, SUM() , AVG().
  
table_name: Name of the table.
  
condition: Condition used.

Eg:

``` sh
SELECT NAME, SUM(SALARY) FROM Employee 
GROUP BY NAME
HAVING SUM(SALARY)>3000; 
``` 

