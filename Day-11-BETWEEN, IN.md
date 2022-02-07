# BETWEEN
The BETWEEN operator selects values within a given range. The values can be numbers, text, or dates. 
The BETWEEN operator includes begin and end values. It can be used in a SELECT, INSERT, UPDATE, or DELETE statement. 

Syntax: 
``` sh 
SELECT column_name(s)
FROM table_name
WHERE column_name BETWEEN value1 AND value2;
``` 

Eg:
 `
SELECT fname, lname
FROM student
WHERE marks BETWEEN 40 AND 80;  `

Eg:
 `
Print all columns between Aman and Emma
SELECT * FROM student
WHERE Name BETWEEN 'Aman’ AND 'Emma'
ORDER BY Name; `

**Using BETWEEN with date values**

eg:
 `
SELECT Fname, Lname
FROM student
where DateOfBirth
BETWEEN '2001-04-20' AND '2001-11-21'; `

**Using NOT operator with BETWEEN**

Syntax:
``` sh
SELECT Fname, Lname
FROM student
WHERE marks
NOT BETWEEN 70 AND 100;
``` 

# IN OPERATOR


IN operator allows you to easily test if the expression matches any value in the list of values. 
It is used to remove the need of multiple OR condition in SELECT, INSERT, UPDATE or DELETE. You can also use NOT IN to exclude the rows in your list.

Syntax: 
 ``` sh
SELECT column_name(s)
FROM table_name
WHERE column_name IN (list_of_values);
``` 

Eg:
 ` Find the Fname, Lname of the students who have marks equal to 40, 65, or 80  `

` SELECT Fname, Lname
FROM student
WHERE marks IN (40, 65, 80); `

Eg: ` Find the Fname, Lname of all the student who have marks not equal to 80 or 90. `

` SELECT Fname, Lname
FROM student
WHERE marks NOT IN (80, 90); `
