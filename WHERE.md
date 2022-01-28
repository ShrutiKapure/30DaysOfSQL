-**WHERE Clause**

The WHERE clause is used to filter records.
It is used to extract only those records that fulfill a specified condition.

SYNTAX:
``` sh
SELECT column1, column2
FROM table_name
WHERE column_name operator value; 
``` 

eg:
` SELECT Name, Age
FROM Student
WHERE Age=10; `

List of operators that can be used with where clause:

>	        Greater Than
>=	      Greater than Equal to
<	        Less Than
<=	      Less than  Equal to
= 	      Equal to
<>	      Not Equal to
BETWEEN	  In an inclusive Range
LIKE	    Search for a pattern
IN	      To specify multiple possible values for a column 

eg: To fetch Name and Age of students with Roll_no less than 10

``` sh
SELECT Name, Age, Roll_no
FROM Student
WHERE Roll_no < 10;

```
**BETWEEN Operator**

The BETWEEN operator selects values within a given range. The values can be numbers, text, or dates.
The BETWEEN operator is includes begin and end values.

SYNTAX:
``` sh
SELECT column1, column2
FROM Student
WHERE column_name
BETWEEN value1 AND value2;
``` 
eg:
` SELECT * FROM Student WHERE Roll_no BETWEEN 1 AND 10; `

LIKE Operator

The LIKE operator is used in a WHERE clause to search for a specified pattern in a column.

There are two sign often used in conjunction with the LIKE operator:

-The percent sign (%) represents zero, one, or multiple characters

-The underscore sign (_) represents one, single character
(You can also combine any number of conditions using AND or OR operators.)

SYNTAX:
' ' 'sh
SELECT column1,column2 
FROM table_name 
WHERE column_name 
LIKE pattern;
' ' '
eg: To fetch records of students where NAME starts with letter S.
` SELECT * FROM Student WHERE NAME LIKE 'S%'; (starting with S) `

` SELECT * FROM Student WHERE NAME LIKE '%AM%'; (AM in any position eg:RAM, RAMESH) `

` SELECT * FROM Student WHERE NAME LIKE '%d'; (ending with d) `

` SELECT * FROM Student WHERE NAME LIKE '_s%'; (s in second position) `

` SELECT * FROM Student WHERE NAME LIKE 'r__%'; (starting with r and are atleast 3) `

` SELECT * FROM Student WHERE NAME LIKE 's%a'; (start s and end a) `

**IN Operator**

The IN operator allows you to specify multiple values in a WHERE clause.
``` sh
Syntax:
SELECT column1,column2 
FROM table_name 
WHERE column_name 
IN (value1,value2,..);
``` sh

Eg: To fetch Name and Roll_no of students where Age is 10 or 12.

` SELECT Name, Roll_no
FROM Student
WHERE Age IN (10,12); `

Eg: To fetch records of students where ROLL_NO is 5 or 10.

` SELECT * FROM Student WHERE Roll_no IN (5,10);`

