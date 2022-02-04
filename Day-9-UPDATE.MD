**UPDATE**
The UPDATE statement is used to modify the existing records in a table.
The UPDATE statement in SQL is used to update the data of an existing table in database.
We can update single columns as well as multiple columns using UPDATE statement as per our requirement.

Syntax:
``` sh
UPDATE table_name 
SET column1 = value1, column2 = value2,... 
WHERE condition;
``` 
table_name: name of the table

column1: name of first , second, third column....

value1: new value for first, second, third column....

condition: condition to select the rows for which the 
           values of columns needs to be updated.

**Updating single column** 

eg:
` UPDATE Student 

SET Name = 'Sharath' WHERE Age = 21; `

**Updating multiple columns**
` UPDATE Student 

SET Name = 'Sharath', Address = 'Malad' WHERE roll_no = 4; `

**Updating whole table**
If we omit the WHERE clause from the update query then all of the rows will get updated. 

` UPDATE Student 

SET Name = ‘Sharath’; `
