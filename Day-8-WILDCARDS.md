**WILDCARDS**

A wildcard character is used to substitute one or more characters in a string. Wildcard characters are used with the LIKE operator. 
The LIKE operator is used in a WHERE clause to search for a specified pattern in a column.

Syntax:
``` sh
SELECT column1,column2 FROM table_name WHERE column LIKE wildcard_operator;
```

column1 , column2: fields in the table

table_name: name of table

column: name of field used for filtering data

eg:
 ` SELECT * FROM Student WHERE NAME LIKE 'S%'; (starting with S) `
 
 ` SELECT * FROM Student WHERE NAME LIKE '%AM%'; (AM in any position eg: RAM, RAMESH) `
 
 ` SELECT * FROM Student WHERE NAME LIKE '%d'; (ending with d) `
 
 ` SELECT * FROM Student WHERE NAME LIKE '_s%'; (s in second position) `
 
 ` SELECT * FROM Student WHERE NAME LIKE 'r__%'; (starting with r and are atleast 3) `
 
 ` SELECT * FROM Student WHERE NAME LIKE 's%a'; (start s and end a) `



