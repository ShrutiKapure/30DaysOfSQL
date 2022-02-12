# DISTINCT Clause

The SELECT DISTINCT statement is used to return only distinct (different) values.

Syntax:
``` sh
SELECT DISTINCT column1, column2 FROM table_name;
``` 

eg:  

 ` SELECT DISTINCT Name, Age 
FROM Student;  `

To fetch unique names from the "Name" field-

 ` SELECT DISTINCT Name
FROM Student;  `

To fetch a unique combination of rows from the whole table –
 
 ` SELECT DISTINCT * 
FROM Student;  `


# AGGREGATE   FUNCTIONS

1) Count()

2) Sum()
 
3) Avg()

4) Min()

5) Max()

**Count()**
 
Returns total number of records .i.e 6.
 
Count(salary): Return number of Non Null values over the column salary. i.e 5.

Count(Distinct Salary):  Return number of distinct Non Null values over the column salary .i.e 4
 
**Sum()**
 
sum(salary):  Sum all Non Null values of Column salary i.e., 310

sum(Distinct salary): Sum of all distinct Non-Null values i.e., 250.
 
**Avg()**
 
Avg(salary) = Sum(salary) / count(salary) = 310/5

Avg(Distinct salary) = sum(Distinct salary) / Count(Distinct Salary) = 250/4
 
**Min()**
 
Min(salary): Minimum value in the salary column except NULL i.e., 40.

**Max()**

Max(salary): Maximum value in the salary i.e., 80.


