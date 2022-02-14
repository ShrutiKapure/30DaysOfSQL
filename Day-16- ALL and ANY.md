# ALL

The ALL operator:

•	returns a boolean value as a result

•	returns TRUE if ALL of the subquery values meet the condition

•	is used with SELECT, WHERE and HAVING statements

ALL means that the condition will be true only if the operation is true for all values in the range. 

ALL Syntax With SELECT

``` sh
SELECT ALL column_name(s)
FROM table_name
WHERE condition;
Eg:
SELECT ALL ProductName
FROM Products
WHERE TRUE;
``` 

ALL Syntax With WHERE or HAVING

``` sh
SELECT column_name(s)
FROM table_name
WHERE column_name operator ALL
  (SELECT column_name
  FROM table_name
  WHERE condition);
  ```
  
Eg:

``` sh
SELECT ProductName 
FROM Products
WHERE ProductID = ALL
 (SELECT ProductID 
FROM OrderDetails 
WHERE Quantity = 10);
``` 

# ANY

The ANY operator:

•	returns a boolean value as a result

•	returns TRUE if ANY of the subquery values meet the condition

ANY means that the condition will be true if the operation is true for any of the values in the range

ANY Syntax

``` sh
SELECT column_name(s)
FROM table_name
WHERE column_name operator ANY
  (SELECT column_name
  FROM table_name
  WHERE condition);
  ``` 

Eg:

``` sh
SELECT ProductName
FROM Products
WHERE ProductID = ANY
  (SELECT ProductID
  FROM OrderDetails
  WHERE Quantity = 10);
  ``` 

*Note: The operator must be a standard comparison operator (=, <>, !=, >, >=, <, or <=).*




