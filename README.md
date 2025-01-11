SQL
=====

SQL Stands for structure Query language. it is a programming language used for manging and manupulating railational databases.


Databases
===========

A database is an organized collection of data stored and accessed electronically. it provides a way to stored, orgainze and retrive large amount of data efficently.


Primery Key
============

A primery key is column or combination of columns that uniquely identifies each row in a table. it enforces the entity integrity rule in a relational database.


Foreign Key
============

A forgin key is column or combinatoion of columns that established a link between data in two tables. it ensures refrential intergity by enforcing relationship betweenn tables.

################## 

1. Create database name
======================

CREATE DATABASE comany;


2. Use select a specific Database to work with

USE company;

3. Alter Database -- Modifyig a database attributes

ALTER DATABASE database_name;

4. Drop database -- delete an existing database

DROP DATABASE company;

5. CREATE -- Create New table, database or index

CREATE TABLE EMPLOYEE( 
  emp_id int PRIMERY KEY,
  first_name VARCHAR(50),
  last_name VARCHAR( 50),
  department VARCHAR( 50),
  salary DECIMAL (10, 2)
);

INSERT INTO employees ( emp_id,first_name, last_name, department, salary)
VALUES
(1, 'John', 'Doe', 'HR', 50000.00),
(2, 'Jane', 'Smith', 'IT', 60000.00),
(3, 'Alice', 'Johnson', 'Finance', 55000.00),
(4, 'Bob', 'Williams', 'IT', 62000.00),
(5, 'Emily', 'Brown', 'HR', 48000.00);

DROP TABLE : delete a table and its data
DROP table employees;

9. SELECT: Retrieve Data From One Or More Tables

select * form emplyees;

10. DISTINCT: Select Unique Values From A Column

slect distinct department from employes;


11. WHERE: Filter Rows Based On Specified Conditions

select * from employees where salary > 550000;

12. LIMIT: Limit The Number Of Rows Returned In The Result Set

select * from employess limit 3;

13. OFFSET: Skip A Specified Number Of Rows Before Returning The Result Set

select * from emplyess offeset 2;


15. CASE: perform conditonal logic in a query
select 
  first_name,
  last_name,
  CASE 
    WHEN SALARY > 55000 THEN 'HIGH'
    WHEN SALARY > 50000 THEN 'MEDIUM'
    ELSE 'LOW'
  END AS salary_category
  FROM emolyess;


16. UPDATE: Modify Existing Records In A Table

UPDATE employees 
SET salary = 55000
where emolyee_id = 1;


17. DELETE: Remove Records From A Table
DELETE from emplyees 
where employee_id = 5;




18. WHERE: Filter Rows based on specific condition 

SELECT * FROM employees where department = 'it'

-- this query will retrive all employees who work in IT department


19. LIKE: match a pattern in a columns

select * from employees where first_name LIKE 'J%';

-- this query will retrive the data of all employees whose first name start with 'j'

20. IN: Match Any Value In A List





