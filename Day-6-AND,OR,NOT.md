# AND ,OR, NOT  Operators

**AND**

This operator displays only those records where both the conditions condition1 and condition2 evaluates to True. 

SYNTAX:
``` sh
SELECT * FROM table_name 
WHERE condition1 and condition2 and…condition; 
```

 Eg: ` SELECT * FROM Student
WHERE Age = 10 AND Address = ‘Mumbai’; `


**OR Operator**

This operator displays the records where either one of the conditions condition1 and condition2 evaluates to True. That is, either condition1 is True or condition2 is True. 

Syntax:
``` sh
SELECT * FROM table_name
WHERE condition1 OR condition2 OR …conditionN;
``` 
Eg: ` SELECT * FROM Student
WHERE Age = 10 OR Age = 5; `


**Combining AND and OR**

Syntax:
``` sh
SELECT * FROM table_name 
WHERE condition1 AND (condition2 OR condition3);
``` 

Eg: ` SELECT * FROM Student
WHERE Age = 10 AND (Name =’Suraj’ OR Name = ‘Sanjay’); `

**NOT Operator**

Syntax:
``` sh
SELECT column1, colomn2, … 
FROM table_name WHERE NOT condition;
``` 
Eg: ` SELECT *FROM Student 
WHERE NOT Age= 10; `

**Combining AND, OR and NOT**

` SELECT * FROM Students 
WHERE NOT Name=’Usha’ AND NOT Name=’Emma’; `

Result: Everything else will be displayed except the condition.

