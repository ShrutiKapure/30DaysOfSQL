**ADD DROP MODIFY**

ALTER TABLE is used to add, delete/drop or modify columns in the existing table. It is also used to add and drop various constraints on the existing table.

**ALTER TABLE – ADD**

ADD is used to add columns into the existing table.

Syntax:
``` sh
 ALTER TABLE table_name
       ADD (Columnname_1  datatype,Columnname_2  datatype,..
              Columnname_n  datatype);
``` 

Eg: ` ALTER TABLE student ADD( Name varchar(50), roll_no number(2)); `

**DROP**

DROP COLUMN is used to drop column in a table. Deleting the unwanted columns from the table.

Syntax:

``` sh
ALTER TABLE table_name
DROP COLUMN column_name;
``` 

Eg:  ` ALTER TABLE student DROP COLUMN roll_no; `

**MODIFY**

It is used to modify the existing columns in a table. Multiple columns can also be modified at once.

*Syntax may vary slightly in different databases.

Syntax(Oracle,MySQL,MariaDB):

``` sh
 ALTER TABLE table_name
MODIFY column_name column_type;
``` 

Eg:  ` ALTER TABLE student MODIFY roll_no number(2); `

Syntax(SQL Server):

``` sh
 ALTER TABLE table_name
ALTER COLUMN column_name column_type;
``` 

Eg:  ` ALTER TABLE student ALTER COLUMN Name varchar(50); ` 

Oracle 10G and later:

``` sh
ALTER TABLE table_name
MODIFY column_name datatype;
``` 

Eg: ` ALTER TABLE student MODIFY name varchar(50); `



