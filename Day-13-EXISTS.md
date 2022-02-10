# EXISTS
The EXISTS operator is used to test for the existence of any record in a subquery. 
The EXISTS operator returns TRUE if the subquery returns one or more records. It can be used in a SELECT, UPDATE, INSERT or DELETE statement.

Syntax:
``` sh
SELECT column_name(s) 
FROM table_name
WHERE EXISTS 
  (SELECT column_name(s) 
   FROM table_name
   WHERE condition);
   ``` 
   
Eg:
 1)	Using EXISTS condition with SELECT statement
 
 ` To fetch the first and last name of the customers who placed atleast one order.
SELECT fname, lname 
FROM Customers 
WHERE EXISTS (SELECT * 
              FROM Orders 
              WHERE Customers.customer_id = Orders.c_id);  `
              

 2)	Using NOT with EXISTS

 ` Fetch last and first name of the customers who has not placed any order.
SELECT lname, fname
FROM Customer
WHERE NOT EXISTS (SELECT * 
                  FROM Orders 
                  WHERE Customers.customer_id = Orders.c_id);
                  

3)	Using EXISTS condition with DELETE statement

 ` Delete the record of all the customer from Order Table whose last name is ‘Patil’.
DELETE 
FROM Orders
WHERE EXISTS (SELECT *
              FROM customers
              WHERE Customers.customer_id = Orders.cid
              AND Customers.lname = 'Patil');
SELECT * FROM Orders;  `



4) Using EXISTS condition with UPDATE statement
 ` Update the lname as ‘Kumari’ of customer in Customer Table whose customer_id is 401.
UPDATE Customers
SET lname = 'Kumari'
WHERE EXISTS (SELECT *
              FROM Customers
              WHERE customer_id = 401);
SELECT * FROM Customers; `

