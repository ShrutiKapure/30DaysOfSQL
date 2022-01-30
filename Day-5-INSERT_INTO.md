**INSERT INTO**

The INSERT INTO statement is used to insert new records in a table.

1) Only value to data to be inserted without column name.
  ``` sh
 INSERT table_name VALUES (value1, value2,…); 
 ``` 
 
Eg:  ` INSERT Student VALUES (4, Sharath, 10); `

2) Column name and value both
``` sh
INSERT table_name (column1, column2,..) VALUES (value1, value2,..);
``` 
Eg:  ` INSERT Student (Roll_no, Name, Age) VALUES (4, Sharath, 10); `

-Using SELECT in INSERT INTO Statement

We can use the SELECT statement with INSERT INTO statement to copy from one table and insert them into another table.

1)	Inserting all columns from a table
``` sh	
INSERT INTO table1
SELECT * FROM table2;
```

Eg:  ` INSERT INTO Student 
SELECT * FROM Student_two; `

2)	Inserting  a specified column.
``` sh		
INSERT INTO table1 ( column_name) 
SELECT column2_name
 FROM table2;
 ``` 
 
Eg: ` INSERT INTO Student (Roll_no, Name, Age) 
SELECT Roll_no, Name, Age 
FROM Student_two;  `

3)	Inserting a specified row.
``` sh
INSERT INTO table1 
SELECT * FROM table2 
WHERE condition;
``` 

Eg:  ` INSERT INTO Student  
SELECT * FROM Student_two 
WHERE Age = 10; `

