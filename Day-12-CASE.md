#CASE
The CASE statement goes through conditions and returns a value when the first condition is me.
So, once a condition is true, it will stop reading and return the result. If no conditions are true, it returns the value in the ELSE clause. 
If there is no ELSE part and no conditions are true, it returns NULL.

Syntax:
``` sh 1)	CASE case_value
    WHEN condition1 THEN result1
    WHEN condition2 THEN result2
    WHEN conditionN THEN resultN
    ELSE result
END;``` 

Eg:
` SELECT FacultyID, Name, Department,
  CASE Gender
  WHEN 'M' THEN 'Male'
  WHEN 'F' THEN 'Female'
END
FROM Faculty  `

Syntax:
``` sh 2)	CASE
    WHEN condition1 THEN result1
    WHEN condition2 THEN result2
    WHEN conditionN THEN resultN
    ELSE result
END CASE ``` 

Eg:
` CASE department_name
 WHEN 'CS'
  THEN UPDATE Faculty SET
  department='Computer Science';
 WHEN 'EC'
  THEN UPDATE Faculty SET
  department='Electronics and Communication';
 ELSE UPDATE Faculty SET
 department='Humanities and Social Sciences';
END CASE  `
