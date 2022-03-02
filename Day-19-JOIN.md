# Join 

# CARTESIAN JOIN:

The CARTESIAN JOIN is also known as CROSS JOIN. 
In a CARTESIAN JOIN there is a join for each row of one table to every row of another table.
This usually happens when the matching column or WHERE condition is not specified.
In the absence of a WHERE condition the CARTESIAN JOIN will behave like a CARTESIAN PRODUCT . 
i.e., the number of rows in the result-set is the product of the number of rows of the two tables.
In the presence of WHERE condition this JOIN will function like a INNER JOIN.
Generally speaking, Cross join is similar to an inner join where the join-condition will always evaluate to True

Syntax:

``` sh
SELECT table1.column1 , table1.column2, table2.column1...
FROM table1
CROSS JOIN table2;
``` 

table1: First table

table2: Second table

Eg:

``` sh
SELECT Student.NAME, Student.AGE, StudentCourse.COURSE_ID
FROM Student
CROSS JOIN StudentCourse;
```

# SELF JOIN

As the name signifies, in SELF JOIN a table is joined to itself.
That is, each row of the table is joined with itself and all other rows depending on some conditions. 
In other words we can say that it is a join between two copies of the same table.

Syntax:

``` sh
SELECT a.coulmn1 , b.column2
FROM table_name a, table_name b
WHERE some_condition;
``` 

table_name: Name of the table.

some_condition: Condition for selecting the rows.

Eg:

``` sh
SELECT a.ROLL_NO , b.NAME
FROM Student a, Student b
WHERE a.ROLL_NO < b.ROLL_NO;
``` 

# INNER JOIN: 

The INNER JOIN keyword selects all rows from both the tables as long as the condition satisfies.
This keyword will create the result-set by combining all rows from both the tables where the condition satisfies i.e value of the common field will be same.

Syntax:

``` sh
SELECT table1.column1,table1.column2,table2.column1,....
FROM table1 
INNER JOIN table2
ON table1.matching_column = table2.matching_column;
``` 

table1: First table.

table2: Second table

matching_column: Column common to both the tables.

*Note: We can also write JOIN instead of INNER JOIN. JOIN is same as INNER JOIN.*

Eg: This query will show the names and age of students enrolled in different courses.

``` sh
SELECT StudentCourse.COURSE_ID, Student.NAME, Student.AGE FROM 
Student
INNER JOIN StudentCourse
ON Student.ROLL_NO = StudentCourse.ROLL_NO;
``` 

# LEFT JOIN: 

This join returns all the rows of the table on the left side of the join and matching rows for the table on the right side of join.
The rows for which there is no matching row on right side, the result-set will contain null. LEFT JOIN is also known as LEFT OUTER JOIN.

Syntax:

``` sh
SELECT table1.column1,table1.column2,table2.column1,....
FROM table1 
LEFT JOIN table2
ON table1.matching_column = table2.matching_column;
``` 

table1: First table.

table2: Second table

matching_column: Column common to both the tables.

*Note: We can also use LEFT OUTER JOIN instead of LEFT JOIN, both are same*

Eg: 
``` sh
SELECT Student.NAME,StudentCourse.COURSE_ID 
FROM Student
LEFT JOIN StudentCourse 
ON StudentCourse.ROLL_NO = Student.ROLL_NO;
``` 

# RIGHT JOIN:

RIGHT JOIN is similar to LEFT JOIN. This join returns all the rows of the table on the right side of 
the join and matching rows for the table on the left side of join. The rows for which there is no matching row on left side, the result-set will contain null.
RIGHT JOIN is also known as RIGHT OUTER JOIN.

Syntax:
``` sh
SELECT table1.column1,table1.column2,table2.column1,....
FROM table1 
RIGHT JOIN table2
ON table1.matching_column = table2.matching_column;
``` 

table1: First table.

table2: Second table

matching_column: Column common to both the tables.

*Note: We can also use RIGHT OUTER JOIN instead of RIGHT JOIN, both are same.*

Eg:

``` sh
SELECT Student.NAME,StudentCourse.COURSE_ID 
FROM Student
RIGHT JOIN StudentCourse 
ON StudentCourse.ROLL_NO = Student.ROLL_NO;
``` 

# FULL JOIN:

FULL JOIN creates the result-set by combining result of both LEFT JOIN and RIGHT JOIN. 
The result-set will contain all the rows from both the tables. The rows for which there is no matching, the result-set will contain NULL values.

Syntax:

``` sh
SELECT table1.column1,table1.column2,table2.column1,....
FROM table1 
FULL JOIN table2
ON table1.matching_column = table2.matching_column;
``` 

table1: First table.

table2: Second table

matching_column: Column common to both the tables.

Eg:
``` sh
SELECT Student.NAME,StudentCourse.COURSE_ID 
FROM Student
FULL JOIN StudentCourse 
ON StudentCourse.ROLL_NO = Student.ROLL_NO;
``` 
