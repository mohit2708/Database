### Table of Contents

|  No.  | Questions                                                                                           |
| :---: | --------------------------------------------------------------------------------------------------- |
|       | [What is database?](#ques-what-is-database)                                                     |
|       | [what is sql?](#ques-Ques-What-is-Sql)                                                              |
|       | [What Is DBMS?](#Ques-What-is-DBMS)                                                                 |
|       | [What Is RDBMS?](#Ques-What-is-RDBMS)                                                               |
|       | [What Is RDBMS?](#Ques-What-is-RDBMS)                                                               |
|       | [Difference between DBMS & RDBMS?](#Ques-Difference-between-DBMS-&-RDBMS)                           |
|       | [What Is Primary Key?](#ques-What-Is-primary-Key)                                                   |
|       | [What Is Unique Key?](#ques-What-Is-Unique-Key)                                                     |
|       | [What Is Foreign Key?](#ques-What-Is-Foreign Key)                                                   |
|       | [Difference between Primary Key & Unique Key?](#ques-Difference-between-Primary-Key-&-Unique-Key)   |
|       | [Difference between Primary Key & Foreign Key?](#ques-Difference-between-Primary-Key-&-Foreign-Key) |
|       | [Difference between Delete, Truncate & Drop?](#ques-Difference-between-Delete,-Truncate-&-Drop)     |
|       | [What Is Joins?](#ques-What-Is-Joins)                                                               |
|       | [Types of Joins?](#ques-Types-of-Joins)                                                             |
|       | [What Is Union & Union All?### What is View](#ques-What-Is-Union-&-Union-All)                       |
|       | [What is View?](#ques-What-is-View)                                                                 |
|       | [What is Index?](#ques-What-is-index)                                                               |
|       |


**[⬆ Back to Top](#table-of-contents)**
### **Ques. What is database?**
* A database is an organized collection of data, stored and retrieved digitally from a remote or local computer system. Databases can be vast and complex, and such databases are developed using fixed design and modeling approaches.
* Database is nothing but an organized form of data for easy access, storing, retrieval and managing of data. 
* This is also known as structured form of data which can be accessed in many ways.


**[⬆ Back to Top](#table-of-contents)**
### **Ques. What Is Sql?**
* SQL is stands for structure query language. It is a database language used for database creation, deletion, fetching rows and modifying rows etc.
* It is a kind of ANSI standard language, used with all database. 

**[⬆ Back to Top](#table-of-contents)**
### **Ques. What Is DBMS?**
* A database management system is program that control creation, maintenance and use of a database.
* DBMS can be termed as File Manager that manages data in a database rather than saving it in ﬁle systems.

**[⬆ Back to Top](#table-of-contents)**
### **What is RDBMS?**
RDBMS stands for Relational Database Management System. RDBMS store the data into the collection of tables, which is related by common fields between the columns of the table. It also provides relational operators to manipulate the data stored into the tables.


**[⬆ Back to Top](#table-of-contents)**
### **Ques. Difference between DBMS & RDBMS?**
| DBMS                                          | RDBMS                                           |
| :-------------------------------------------- | :---------------------------------------------- |
| DBMS applications store data as file          | RDBMS applications store data in a tabular form |
| Normalization is not present in DBMS          | Normalization is present in RDBMS               |
| DBMS does not support distributed data hnbase | RDBMS support distributed database              |

**[⬆ Back to Top](#table-of-contents)**
### **Ques. What are Constraints in SQL?**
Constraints are used to specify the rules concerning data in the table. It can be applied for single or multiple fields in an SQL table during the creation of the table or after creating using the ALTER TABLE command. The constraints are:<br>
* __NOT NULL__ - Restricts NULL value from being inserted into a column.
* __CHECK__ - Verifies that all values in a field satisfy a condition.
* __DEFAULT__ - Automatically assigns a default value if no value has been specified for the field.
* __UNIQUE__ - Ensures unique values to be inserted into the field.
* __INDEX__ - Indexes a field providing faster retrieval of records.
* __PRIMARY KEY__ - Uniquely identifies each record in a table.
* __FOREIGN KEY__ - Ensures referential integrity for a record in another table.

**[⬆ Back to Top](#table-of-contents)**
### **Ques. What Is Primary Key?**
* The PRIMARY KEY constraint uniquely identifies each record in a database table. It must contain unique values. A Primary Key column cannot have Null values.
* A table can have only one primary key, which may consist of single or multiple fields. When multiple fields are used as a primary key, they are called a composite key.<br>
__Create Primary Key:-__ <br>
__Type 1.__<br>
```sql
CREATE TABLE emp
     (
Emp_ID INT  primary key,
Emp_name Varchar(100),
Emp_Sal Decimal (10,2)
      )
```
__Type 2.__
```sql
CREATE TABLE emp
      (
Emp_ID INT,
Emp_name Varchar(100),
Emp_Sal Decimal (10,2),
primary key (emp_id)
       )
```
__Delete primary Key__
```sql
ALTER TABLE CUSTOMERS DROP PRIMARY KEY;
```
__Add primary Key__
```sql
ALTER TABLE table_name ADD PRIMARY KEY (Id)
```

**[⬆ Back to Top](#table-of-contents)**
### **Ques. What Is Unique Key?**
* A unique key is a set of one or more than one fields/columns of a table that uniquely identify each record in a database table.
* The Unique and Primary Key constraints both provide a guarantee for a column or set of columns.
* A Primary Key consist automatically has a unique constraint define on it.

**[⬆ Back to Top](#table-of-contents)**
### **Ques. What Is Foreign Key?**
* A foreign key is a key used to link two tables together. This is something called a reference key.
* Foreign key is a column or a combination of columns whose values match a primary key in a different table.
* The relationship between two tables matches the primary key in one of the tables with a foreign key in the second table.

**[⬆ Back to Top](#table-of-contents)**
### **Ques. Difference between Primary Key & Unique Key?**
| Primary Key                                                                                                       | Unique Key                                                           |
| :---------------------------------------------------------------------------------------------------------------- | :------------------------------------------------------------------- |
| A table can have only one primary key                                                                             | A table can have more than one unique key                            |
| It does not allow null values                                                                                     | Allows null values                                                   |
| Primary key Can be made foreign key into another table                                                            | In SQL server, unique key Can be made foreign key into another table |
| By default it adds a clustered index                                                                              | By default it adds a unique non-clustered index                      |
| We can generate ID automatically with the help of auto increment field. Primary key support auto increment value. | Unique constraint does not support auto increment value.             |


**[⬆ Back to Top](#table-of-contents)**
### **Ques. Difference between Primary Key & Foreign Key?**
| Primary Key                                            | Foreign Key                                                              |
| :----------------------------------------------------- | :----------------------------------------------------------------------- |
| A table can have only one primary key                  | A table can have more than one foreign key                               |
| Primary key uniquely identified  a record in the table | Foreign key is a field in the table that is primary key in another table |
| It does not allow null values                          | Allows null values                                                       |
| Duplicate not allowed                                  | Duplicate allowed                                                        |
|                                                        | Foreign key do not automatically create an index.                        |

**[⬆ Back to Top](#table-of-contents)**
### **Ques. Difference between Delete, Truncate & Drop?**
| Delete                                                | Truncate                                                       | Drop                  |
| :---------------------------------------------------- | :------------------------------------------------------------- | :-------------------- |
| Delete is a DML command                               | Truncate is DDL command                                        |                       |
| We can use where clause in delete command             | We cannot use where clause with truncate                       |                       |
| Delete statement is used to delete a row from a table | Truncate statement is used to remove all the row from a table  | Remove table and data |
| You can rollback data after using delete statement    | It is not possible to rollback after using TRUNCATE statement. | Can’t rollback        |
| Delete is slower                                      | Truncate is faster                                             |                       |

**[⬆ Back to Top](#table-of-contents)**
### Ques. **What Is Joins?**
SQL Joins are used to combine rows from two or more tables.
```sql
Customers table:                                      
+----+----------+-----+-----------+----------+        
| ID | NAME     | AGE | ADDRESS   | SALARY   |        
+----+----------+-----+-----------+----------+        
|  1 | Ramesh   |  32 | Ahmedabad |  2000.00 |        
|  2 | Khilan   |  25 | Delhi     |  1500.00 |        
|  3 | kaushik  |  23 | Kota      |  2000.00 |        
|  4 | Chaitali |  25 | Mumbai    |  6500.00 |        
|  5 | Hardik   |  27 | Bhopal    |  8500.00 |   
|  6 | Komal    |  22 | MP        |  4500.00 |
|  7 | Muffy    |  24 | Indore    | 10000.00 |
+----+----------+-----+-----------+----------+
Order table:
+-----+---------------------+-------------+--------+
|OID  | DATE                | CUSTOMER_ID | AMOUNT |
+-----+---------------------+-------------+--------+
| 102 | 2009-10-08 00:00:00 |           3 |   3000 |
| 100 | 2009-10-08 00:00:00 |           3 |   1500 |
| 101 | 2009-11-20 00:00:00 |           2 |   1560 |
| 103 | 2008-05-20 00:00:00 |           4 |   2060 |
+-----+---------------------+-------------+--------+
```
Now, let us join these two tables in our SELECT statement as follows:
```sql
SQL> SELECT  ID, NAME, AMOUNT, DATE
   FROM CUSTOMERS
   INNER JOIN ORDERS
   ON CUSTOMERS.ID = ORDERS.CUSTOMER_ID;
```
Result:
```sql
+----+----------+-----+--------+
| ID | NAME     | AGE | AMOUNT |
+----+----------+-----+--------+
|  3 | kaushik  |  23 |   3000 |
|  3 | kaushik  |  23 |   1500 |
|  2 | Khilan   |  25 |   1560 |
|  4 | Chaitali |  25 |   2060 |
+----+----------+-----+--------+
```

### **Ques. Types of Joins?**

__Left Joins :-__ Returns all rows from the left table, even if there are no matches in the right table.<br>
Table 1 − CUSTOMERS Table
```sql
+----+----------+-----+-----------+----------+ 
| ID | NAME     | AGE | ADDRESS   | SALARY   |
+----+----------+-----+-----------+----------+
|  1 | Ramesh   |  32 | Ahmedabad |  2000.00 |
|  2 | Khilan   |  25 | Delhi     |  1500.00 |
|  3 | kaushik  |  23 | Kota      |  2000.00 |
|  4 | Chaitali |  25 | Mumbai    |  6500.00 |
|  5 | Hardik   |  27 | Bhopal    |  8500.00 |
|  6 | Komal    |  22 | MP        |  4500.00 |
|  7 | Muffy    |  24 | Indore    | 10000.00 |
+----+----------+-----+-----------+----------+
```
Table 2 − Orders Table
```sql
+-----+---------------------+-------------+--------+
| OID | DATE                | CUSTOMER_ID | AMOUNT |
+-----+---------------------+-------------+--------+
| 102 | 2009-10-08 00:00:00 |           3 |   3000 |
| 100 | 2009-10-08 00:00:00 |           3 |   1500 |
| 101 | 2009-11-20 00:00:00 |           2 |   1560 |
| 103 | 2008-05-20 00:00:00 |           4 |   2060 |
+-----+---------------------+-------------+--------+
```
```sql
SQL> SELECT  ID, NAME, AMOUNT, DATE
   FROM CUSTOMERS
   LEFT JOIN ORDERS
   ON CUSTOMERS.ID = ORDERS.CUSTOMER_ID;
```
Result:-
```sql
+----+----------+--------+---------------------+
| ID | NAME     | AMOUNT | DATE                |
+----+----------+--------+---------------------+
|  1 | Ramesh   |   NULL | NULL                |
|  2 | Khilan   |   1560 | 2009-11-20 00:00:00 |
|  3 | kaushik  |   3000 | 2009-10-08 00:00:00 |
|  3 | kaushik  |   1500 | 2009-10-08 00:00:00 |
|  4 | Chaitali |   2060 | 2008-05-20 00:00:00 |
|  5 | Hardik   |   NULL | NULL                |
|  6 | Komal    |   NULL | NULL                |
|  7 | Muffy    |   NULL | NULL                |
+----+----------+--------+---------------------+
```
* Inner join: Inner join return rows when there is at least one match of rows between the tables.
* Right Join: Right join return rows which are common between the tables and all rows of Right hand side table. Simply, it returns all the rows from the right hand side table even though there are no matches in the left hand side table.
* Full join: return rows when there are matching rows in any one of the tables.
* Self Join:- It is used to join one single table with itself as there were two different tables.
* Cross join:- This is the basic join, it is nothing but a cartesian product. This join method compares every single row of a table with every single row of the other table.



**[⬆ Back to Top](#table-of-contents)**
### **Ques. What Is Union & Union All?**
__Ans.__ Both UNION and UNION ALL Operator combine rows from result sets into a single result set. 


**[⬆ Back to Top](#table-of-contents)**
### **Ques. Difference between Union & Union All?**
| Union                                                     | Union All                                     |
| :-------------------------------------------------------- | :-------------------------------------------- |
| Union removes duplicate rows.                             | Union All does not remove the duplicate rows. |
| Union uses a distinct sort                                | Union All does not use a distinct sort        |
| Union can’t work with a column that has a text data type. | Union All can work with all data type column. |
```sql
Select Column1, Column2, Column3 from Table A
UNION
Select Column1, Column2, Column3 from Table B
--------------------------------------------------
Select Column1, Column2, Column3 from Table A
UNION ALL
Select Column1, Column2, Column3 from Table B
```


**[⬆ Back to Top](#table-of-contents)**
### **What is View?**
* A view can contain all rows of a table or select rows from a table. A view can be created from one or many tables which depends on the written SQL query to create a view
* It is a kind of logical table, having no own data.
* A view is a virtual table which consists of a subset of data contained in a table. Views are not virtually present, and it takes less space to store. View can have data of one or more tables combined, and it is depending on the relationship.

__Syntax:-__
```sql
         Create view view_name
         As
        Select column1, column2
        From  table_name  
       Where [condition];
```
__Show view__
```sql
SELECT * FROM CUSTOMERS_VIEW;
```

**[⬆ Back to Top](#table-of-contents)**
### **What is Index?**
* An index is used to enhance the performance of SQL Queries.
* It will get the data using Row Id, avoid full table scan.
* A database index is a data structure that improves the speed of operation in a table.
* index can be created one or more columns.
* Index allows the database application to find data fast, without reading the whole table.
* An index can be created in a table to find data more quickly and efficiently.
```sql
CREATE INDEX KAKA 
    ON EMP(EMPNO) 
    SELECT * FROM EMP WHERE EMPNO=7788 (FAST ACCESS)
```
__Types of index__
__cluster index:-__ jab kisi table par hum primary key lagate hai to wo cluster index ban jata hai..
__Non cluster index:-__ table mai jis column par select command sabse jyda chalte hai to us column par hum non cluster index bna lete hai.

**[⬆ Back to Top](#table-of-contents)**
### **What is Cursor?**
* WHEN WE USE SELECT STMT IN DATABASE(ORACLE/SQLSERVER/MYSQL) ,   it allocate memory for that known as cursor.
* A cursor is a pointer to this context area. PL/SQL controls the context area through a Cursor.
* A Cursor can hold more than one row, but can process only one row at a time. The set of rows the cursor hold is called the active set.
* A cursor is a temporary work area created in the system memory when a SQL statement is executed. A cursor contains information on a select statement and the rows of data accessed by it.
* This temporary work area is used to store the data retrieved from the database and manipulate this data.

#### There are two type of cursor in PL/SQL:-

1. **Implicit cursor:-**
   * These are creating by default when DML statement like, INSERT, UPDATE, and DELETE statement are executed. They are also created when a SELECT statement that returns just one row is executed.
   * Implicit cursors are automatically created by oracle whenever an SQL statement is executed, when there is no explicit cursor for the statement. Programmers cannot control the implicit cursor and the information in it.

**[⬆ Back to Top](#table-of-contents)**
### **What is Trigger?**
* • Trigger  are set of structure Query language (SQL) statement that perform particular task. They invoke specific event (after Insert,u,d – before I,u,d)
* Database triggers are sets of commands that get executed when an event (Before Insert, After Insert, On Update, on delete of a row) occurs on a table.
* Triggers are special type of stored procedures that are defined to execute automatically in place or after data modification.
* Trigger allows you to execute a batch of SQL code an insert, update or delete command is execute against a specific table.
```sql
CREATE OR REPLACE TRIGGERRESTRICT_EMP
BEFORE INSERT ON EMP
BEGIN
RAISE_APPLICATION_ERROR(-20987,’INSERT MAT KAR NAHI HOGA’);
END;
```

### Difference between WHERE and HAVING in SQL?
| Having                                                           | Where                                                                      |
| :--------------------------------------------------------------- | :------------------------------------------------------------------------- |
| Having ke sath GROUP BY use hota hai                             |                                                                            |
| Having post filter hai(data fatch hone ke baad filter lagta hai) | where pre filter hai(isme pahle filter lagta hai phir fatch data hota hai) |
| having can be used only with select command                      | can be used with select update delete                                      |
| HAVING is used for column operations.                            | WHERE is used for row operations                                           |
| having ke aggrigate function sath kar sakte hai                  | where ke sath aggrigate function use nahi kar sakte                        |
```sql
a   c1  40
a   c2  50
b   c3  30
c   c1  20

select std, sum(score) as total from record group by std having total>60;
```


### **Ques. Difference between Group By And Order By?**
__Group By:-__ It is used to group our result sets of tables in a database and is often used with Count, Sum, avg etc. 
```sql
Ex:- Select COUNT(state), country from emp group by country.
```
__Order By:-__ It changes only order in our result set i.e sorting
```sql
Ex:- Select COUNT(state), country from emp order by country_id..
```

### **List of Mysql storage Engines/Table Type?**
Mysql ne apni requirment ke according alag-alag table type diye hai.
1. MyIsam:-
* Myisam good for select command.
* it support full text searching.
* it support table level locking.
* it support Blob and text column can be indexed.
2. Innodb
* it support for referential integrity.
* it support foreign key constraint.
* it support Row level locking.
* it support for transaction. 
3. CSV
* The CSV storage engine stores data in text file using comma separated values format.
4. Archive
5. memory 
6. black hole
7. merge
8. federated


### **Ques. What is Stored procedure?**
* Stored procedure is a function which cantains a collection of sql quries, the procedure can take inputs, process them and send back output.
* Stored procedure is a database object which is used to perform some specific task.
* Stored procedure is called explicitly.
* Store procedures is set of structure Query language (SQL) statement that perform particular task.
* Store procedures is set of structure Query language (SQL) statement with an assigned name, which are stored in a relation database 
management system as a group, so it can be reused and shered by multipal program.
* Advantage: Stored Procedures are precompiled and stored in the database. This enables the Database to execute the queries much faster. Since many queries can be included in a stored procedure, round trip time to execute multiple queries from source code to
Database and back is avoided.
* A procedure is a group of SQL statement that you can call by name.
* Store procedures is a database object which is used to perform some specific task.

__Advantage__
* Store procedure is reducing the complexity of code in code behind.
* Store procedures have repeatedly having data. It helps to reuse the code.
* It store in precompiled format so execution of speed is much faster than SQL statement.

```
1. Store procedures explicitly call hote hai.
2. Tiger automatic call hote hai.
3. Function inside the sql call hote hai.
```

```sql
create procedure procedure_name as
begain
  select name, age from emp;
end

execute procedure_name
```

```sql
CREATE OR REPLACE PROCEDURE ABCD
IS 
BEGIN
DBMS_OUTPUT.PUT_LINE('JAI PL BABA');
END;
sql>EXECUTE ABCD (sql>set serveroutput on)
```
```sql
ALTER procedure [dbo].[inemp]
@eno int,@enm varchar(20),@sl int
as
begin
insert into emp(EMPNO,ENAME,SAL) values(@eno,@enm,@sl);
end
```

### **Ques. What is the normalization?**
* In database design, we start with one single table, with all possible columns. A lot of redundant data would be present since it’s a single table. The process of removing the redundant data, by splitting up the table in a well deﬁned fashion is called
normalization.
* Normalization is the process of minimizing redundancy and dependency by organizing fields and table of a database. The main aim of Normalization is to add, delete or modify field that can be made in a single table.
* A lot of redundant data would be present since it’s a single table. The process of removing the redundant data, by splitting up the table in a well defined fashion is called normalization.

### **Ques. What are types of normalization?**
1. **First Normal Form (1NF):-** A relation is said to be in ﬁrst normal form if and only if all underlying domains contain atomic values only. After 1NF, we can still have redundant data.
2. **Second Normal Form (2NF):-** A relation is said to be in 2NF if and only if it is in 1NF and every non key attribute is fully dependent on the primary key. After 2NF, we can still have redundant data.
3. **Third Normal Form (3NF):-** A relation is said to be in 3NF, if and only if it is in 2NF and every non key attribute is non-transitively dependent on the primary key.

```
**Types of normalization:**
A. First normal form (1NF): This should remove all the duplicate columns from the table.
Creation of tables for the related data and identification of unique columns.
B. Second normal form (2NF): Meeting all requirements of the first normal form. Placing the
subsets of data in separate tables and Creation of relationships between the tables using
primary keys
C. Third normal form (3NF): This should meet all requirements of 2NF. Removing the columns
0which are not dependent on primary key constraints.
D. Fourth normal form (4NF): Meeting all the requirements of third normal form and it should
not have multi- valued dependencies.
```

### **Ques. What is Json?**
* Json stands for Javascript Object Notation and Json is lightweight data interchange format.
* Json is syntax for storing and exchanging data.
* it is easy for machine to parse and recreates.
* Json is often used when data is sent from a server to a web page.

__JSON Advantage__
* JSON does not have namespace.
* JSON is not extensible.


# **Sql Query:-**
#### Create database
```sql
create database <databse_name>
```
#### Rename database
```sql
ALTER DATABASE old_datbase MODIFY = new_database
```
#### Delete database
```sql
drop database mohit
```

#### Create table
```sql
CREATE TABLE table_name
(
id int AUTO_INCREMENT primary key, 
column_name1 data_type(size),
column_name2 data_type(size),
column_name3 data_type(size),
..
);
```

#### Rename Table
```sql
RENAME TABLE tbl_name TO new_tbl_name
```

#### 2nd highest salary?
* __Using Subquery:-__
```sql
Using Limit:-
SELECT salary
FROM (SELECT salary FROM employees ORDER BY salary DESC LIMIT 2) AS Emp ORDER BY salary LIMIT 1;
```
```sql
SELECT MAX(salary) FROM employees WHERE salary NOT IN ( SELECT Max(salary) FROM employees); (OR)
SELECT MAX (SAL) FROM EMP WHERE SAL < (SELECT MAX (SAL) FROM EMP);
```

```sql
Using Sub query and < operator instead of IN clause:-
SELECT MAX(salary)
From employees
WHERE salary < ( SELECT Max(salary) FROM employees);
```

#### Ques. Department wise highest Salary?
| deptno | sal  |
| :----- | :--- |
| 10     | 5000 |
| 30     | 4000 |
| 10     | 2000 |
| 20     | 2000 |
| 20     | 3000 |
| 20     | 1000 |
```sql
SELECT Deptno, MAX(Sal) FROM EmpDetails GROUP BY Deptno;
|deptno|sal|
|10|5000|
|30|4000|
|20|3000|
```

#### Ques. 3rd highest salary?
```sql 
SELECT MAX (SAL) FROM EMP WHERE SAL &lt; (SELECT MAX (SAL) FROM EMP WHERE
SAL &lt; (SELECT MAX (SAL) FROM EMP))
```

### Ques. 5th highest salary?
```sql
SELECT Max(SAL) FROM(SELECT DISTINCT SAL FROM EMP WHERE SAL IS NOT NULL  ORDER BY SAL DESC)WHERE ROWNUM <6;
select * from emp order by salery desc limit 4(5th postion),1(no of records);
```

### Ques. Top Salery?
```sql
select * from emp where sal = (select max(salery) from emp);
```
### Ques. How to copy a table in another table?
```sql
CREATE TABLE EMP1 AS (SELECT * FROM EMP); //constraint will not copied.
```
### Ques. How to copy structure of a table but not data?
```sql
CREATE TABLE STD AS (SELECT * FROM EMP WHERE EMPNO=-1);
```












MySql Interview Questions



Ques. Difference between inner & self & cross ?
Ans. 
Inner:-
Self:-
Cross:-




Json:-
Json stands for Javascript Object Notation and Json is lightweight data interchange format.
Json is syntax for storing and exchanging data.
it is easy for machine to parse and recreates.
Json is often used when data is sent from a server to a web page.


Ques. Find Names of students whose age is greater than 21 ?
Ans. Select [student_name] from [student_tbl] where [student_age] < 21


SQL Queries:-
-------?
Oracle
SQL
Top 5 Salary
SELECT SAL FROM(SELECT DISTINCT SAL FROM EMP WHERE SAL IS NOT NULL  ORDER BY SAL DESC)WHERE ROWNUM <6;
select top 5 sal from saxena order by sal desc;
select * from emp order by salery desc limit 5;


Delete table
Delete table_name; (only table data del)drop table persons;
drop table persons;
Insert data in a table or a  particular column


INSERT INTO emp VALUES (001,'saxena','mohit','mainpuri','mnq')
SQL>INSERT INTO emp(EMPNO,ENAME) VALUES(2,'DDDD');
INSERT INTO Persons VALUES (001,'saxena','mohit','mainpuri','mnq')


Create a table from another table
CREATE TABLE JOLLY AS SELECT * FROM EMP;  //constraint will not copy(pk,uk..)




Copy structure of table not data
CREATE TABLE JOLLY AS (SELECT * FROM EMP WHERE EMPNO=-1);




Insert data in another table

Add column
ALTER TABLE table_name
ADD column_name datatype(size), column_name datatype(size));
ALTER TABLE table_name
ADD column_name datatype
Rename column
ALTER TABLE table_name RENAME COLUMN old_name to new_name;
exec sp_rename 'persons.idproof' , 'idn','column'
Delete column
ALTER TABLE table_name
DROP COLUMN column_name;
ALTER TABLE table_name
DROP COLUMN column_name


Data insert/update in a column
update emp set city='noida' where lastname='saxena'
update emp set city='noida' where lastname='saxena'
Rename Datatype
ALTER TABLE LALU MODIFY (MOBILE NUMBER(15));


Row delete
delete from table_name where ID=01;
delete from table_name where ID IN(2,6);
Current date


select GETDATE();


CREATE TABLE mohit
       (EMPNO numaric(4) CONSTRAINT pk_emp PRIMARY KEY,
        ENAME VARCHAR(10),
        JOB VARCHAR(9),
        MGR numaric(4),
        HIREDATE DATE,
        SAL numaric(7, 2),
        COMM numaric(7, 2),
        DEPTNO numaric(2) CONSTRAINT fk_emp_dept REFERENCES dept(deptno))
select * from saxena
INSERT INTO saxena VALUES
        (7369, 'SMITH',  'CLERK', 7902,'17-DEC-1980',  800, NULL, 20);
INSERT INTO saxena VALUES
        (7499, 'ALLEN',  'SALESMAN',  7698,'20-FEB-1981',1600,  300, 30);
INSERT INTO saxena VALUES
        (7521, 'WARD',   'SALESMAN',  7698,'22-FEB-1981', 1250,  500, 30);
INSERT INTO saxena VALUES
        (7566, 'JONES',  'MANAGER',   7839,'2-APR-1981', 2975, NULL, 20);
INSERT INTO saxena VALUES
        (7654, 'MARTIN', 'SALESMAN',  7698,'28-SEP-1981', 1250, 1400, 30);
INSERT INTO saxena VALUES
        (7698, 'BLAKE',  'MANAGER',   7839,'1-MAY-1981',  2850, NULL, 30);
INSERT INTO saxena VALUES
        (7782, 'CLARK',  'MANAGER',   7839,'9-JUN-1981', 2450, NULL, 10);
INSERT INTO saxena VALUES
        (7788, 'SCOTT',  'ANALYST',   7566,'09-DEC-1982', 3000, NULL, 20);
INSERT INTO saxena VALUES
        (7839, 'KING',   'PRESIDENT', NULL,'17-NOV-1981', 5000, NULL, 10);
INSERT INTO saxena VALUES
        (7844, 'TURNER', 'SALESMAN',  7698,'8-SEP-1981',  1500,    0, 30);
INSERT INTO saxena VALUES
        (7876, 'ADAMS',  'CLERK',     7788,
        '12-JAN-1983', 1100, NULL, 20);
INSERT INTO saxena VALUES
        (7900, 'JAMES',  'CLERK',     7698,
        '3-DEC-1981',   950, NULL, 30);
INSERT INTO saxena VALUES
        (7902, 'FORD',   'ANALYST',   7566,
      '3-DEC-1981',   3000, NULL, 20);
INSERT INTO saxena VALUES
        (7934, 'MILLER', 'CLERK',7782,'23-JAN-1982', 1300, NULL, 40);




5. What are the subsets of SQL?
 Data definition language(DDL)
 Create
 Alter
 Drop
 Rename
 Truncate
 Data manipulation language(DML)
 Insert
 Update
 Delete
 Data control language(DCL)
 Grant: It gives a privilege to user.
 Revoke: It takes back privileges granted from user.



9. What is Denormalization?
DeNormalization is a technique used to access the data from higher to lower normal
forms of database. It is also process of introducing redundancy into a table by
incorporating data from the related tables.


Types of Index:
A. Unique Index: This indexing does not allow the field to have duplicate values if the column
is unique indexed. Unique index can be applied automatically when primary key is defined.
B. Cluster Index: This type of index reorders the physical order of the table and search based
on the key values. Each table can have only one clustered index.
C. Non Cluster Index: Non Clustered Index does not alter the physical order of the table and
maintains logical order of data. Each table can have 999 non clustered indexes.

12. What is the difference between cluster and non cluster index?
A clustered index reorders the way records in the table are physically stored. There can be only
one clustered index per table. It makes data retrieval faster.
A non clustered index does not alter the way it was stored but creates a completely separate
object within the table. As a result insert and update command will be faster.

13. What are set operators in SQL?

4

Union, intersect and minus operator are called set operators.
### Ques. What is ACID property?
* ACID property is used to ensure that the data transactions are processed reliably in a database system.
* A single logical operation of a data is called transaction.
* ACID is an acronym for Atomicity, Consistency, Isolation, and Durability. 
__Atomicity:__<br>
* It requires that each transaction is all or nothing. It means if one part of the transaction fails, the entire transaction fails and the database state is left unchanged.
* A transaction consists of many steps. When all the steps in a transaction get completed, it will get reflected in DB or if any step fails, all the transactions are rolled back.
__Consistency:__
* The consistency property ensures that the data must meet all validation rules. In simple words you can say that your transaction never leaves your database without completing its state.
* The database will move from one consistent state to another, if the transaction succeeds and remain in the original state, if the transaction fails.
Isolation:
 This property ensures that the concurrent property of execution should not be met. The
main goal of providing isolation is concurrency control.
 Every transaction should operate as if it is the only transaction in the system.
Durability:
 Durability simply means that once a transaction has been committed, it will remain so,
come what may even power loss, crashes or errors.
 Once a transaction has completed successfully, the updated rows/records must be
available for all other transactions on a permanent basis

15. What are types of locks?
1. Sheared lock: When a shared lock is applied on data item, other transactions can only read the
item, but can&#39;t write into it.
2. Exclusive lock: When an exclusive lock is applied on data item, other transactions can&#39;t read or
write into the data item.
16. How to delete duplicate record from a table?
SQL&gt;DELETE FROM EMP WHERE ROWID NOT IN (SELECT MAX (ROWID) FROM EMP GROUP BY
ROLL)




| Ques.                                              | Oracle                                                                                                                                                    | SQL                                                                                                                                                                                               | My Sql                                                                                                                                                                                          |
| -------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| __Check version__                                  |                                                                                                                                                           |                                                                                                                                                                                                   | 1.select version() <br> 2.SHOW VARIABLES LIKE "%version%";                                                                                                                                      |
| __Top 5 Salary__                                   | SELECT SAL FROM(SELECT DISTINCT SAL FROM EMP WHERE SAL IS NOT NULL  ORDER BY SAL DESC)WHERE ROWNUM <6;                                                    | select top 5 sal from saxena order by sal desc;                                                                                                                                                   | SELECT  slaery FROM emp ORDER BY slaery DESC LIMIT 2                                                                                                                                            |
| __5th highest salary__                             | SELECT Max(SAL) FROM(SELECT DISTINCT SAL FROM EMP WHERE SAL IS NOT NULL  ORDER BY SAL DESC)WHERE ROWNUM <6;                                               |                                                                                                                                                                                                   | select * from emp group by slaery order by slaery desc limit n-1,1                                                                                                                              |
| __Sub query__                                      |                                                                                                                                                           |                                                                                                                                                                                                   | select sal from emp where sal = (select max(sal) from emp  where sal <> (select max(sal) from emp))                                                                                             |
| __Select max sal all__                             |                                                                                                                                                           |                                                                                                                                                                                                   | select * from emp where salery=(select max(salery) from emp);                                                                                                                                   |
| __Rename database__                                |                                                                                                                                                           | ALTER DATABASE old_datbase MODIFY = new_database                                                                                                                                                  |
| __Create table__                                   | CREATE TABLE table_name <br> ( <br> column_name1 data_type(size), <br> column_name2 data_type(size), <br> column_name3 data_type(size), <br> .... <br> ); | CREATE TABLE table_name <br> ( <br> id int AUTO_INCREMENT primary key, <br> column_name1 data_type(size), <br> column_name2 data_type(size), <br> column_name3 data_type(size), <br> .... <br> ); | CREATE TABLE table_name <br> ( <br> id int AUTO_INCREMENT primary key, <br> column_name1 data_type(size), <br> column_name2 data_type(size), <br> column_name3 data_type(size), <br> .. <br> ); |
| __Rename table__                                   | ALTER TABLE old_table_name rename to new_table_name;                                                                                                      | exec sp_rename 'old table_name','newtable name' <br> RENAME TABLE tbl_name TO new_tbl_name                                                                                                        | RENAME TABLE tbl_name TO new_tbl_name                                                                                                                                                           |
| __Delete table__                                   | Delete table_name; (only table data del)drop table persons;                                                                                               | drop table persons;                                                                                                                                                                               | drop table persons;                                                                                                                                                                             |
| __Insert data in a table or a  particular column__ | INSERT INTO emp VALUES (001,'saxena','mohit','mainpuri','mnq') <br> SQL>INSERT INTO emp(EMPNO,ENAME) VALUES(2,'DDDD');                                    | INSERT INTO Persons VALUES (001,'saxena','mohit','mainpuri','mnq') <br> INSERT INTO table_name (column1,column2,column3,...) VALUES ('value1','value2','value3',...);                             | INSERT INTO table_name (column1,column2,column3,...) VALUES ('value1','value2','value3',...);                                                                                                   |
| __Create a table from another table__              | CREATE TABLE JOLLY AS SELECT * FROM EMP;  //constraint will not copy(pk,uk..)                                                                             |                                                                                                                                                                                                   | CREATE TABLE JOLLY AS SELECT * FROM EMP;                                                                                                                                                        |
| __Copy structure of table not data__               | CREATE TABLE JOLLY AS (SELECT * FROM EMP WHERE EMPNO=-1);                                                                                                 |                                                                                                                                                                                                   | CREATE TABLE JOLLY AS SELECT * FROM EMP WHERE EMPNO=-1;                                                                                                                                         |




