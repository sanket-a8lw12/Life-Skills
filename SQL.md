# SQL
**SQL stands for Structured Query Language. It is a standard language for accessing and manipulating databases. It lets you access and manipulate databases.**

# WHY SQL..?

* The basic use of SQL for data professionals and SQL users is to insert, update, and delete the data from the relational database.

* SQL allows the data professionals and users to retrieve the data from the relational database management systems.

* It allows SQL users to create, drop, and manipulate the database and its tables.

* It also helps in creating the view, stored procedure, and functions in the relational database.

# SQL Commands

The SQL commands help in creating and managing the database. The most common SQL commands which are highly used are mentioned below:

* CREATE command
* UPDATE command
* DELETE command
* SELECT command
* DROP command
* INSERT command

## CREATE command

This command helps in creating the new database, new table, table view, and other objects of the database.

**Example**
```
{
    CREATE TABLE table_name (
        column1 datatype,
        column2 datatype,
        column3 datatype,
    );
}
```

## UPDATE command

This command helps in updating or changing the stored data in the database.

**Syntax**
```
{  
    UPDATE table_name
    SET column1 = value1, column2 = value2, ...
    WHERE condition;
}
```
**Example**
```
{
    UPDATE employees
    ET salary = 50000, department = 'IT'
    WHERE employee_id = 123;
}
```

## DELETE command

This command helps in removing or erasing the saved records from the database tables. It erases single or multiple tuples from the tables of the database.

**Syntax**
```
{   
    DELETE FROM table_name
    WHERE condition;
}
```
**Example**
```
{
    DELETE FROM customers
    WHERE customer_id = 123;
}
```

## SELECT command

This command helps in accessing the single or multiple rows from one or multiple tables of the database. We can also use this command with the WHERE clause.

**Syntax**
```
{   
    SELECT column1, column2, ...
    FROM table_name
    WHERE condition
    GROUP BY column1, column2, ...
    HAVING condition
    ORDER BY column1, column2, ...
}
```
**Example**
```
{
    SELECT first_name, last_name, age
    FROM employees
    WHERE department = 'IT'
    ORDER BY last_name ASC;
}
```

## DROP command

This command helps in inserting the data or records into the database tables. We can easily insert the records in single as well as multiple rows of the table.

**Syntax**
```
{   
    DROP DATABASE database_name;
}
```
**Example**
```
{
    DROP DATABASE employee;
}
```


## INSERT command

This command helps in deleting the entire table, table view, and other objects from the database.

**Syntax**
```
{   
    INSERT INTO table_name (column1, column2, ...)
    VALUES (value1, value2, ...);

}
```
**Example**
```
{
    INSERT INTO employees (first_name, last_name, age)
    VALUES ('John', 'Doe', 30);

}
```



# SQL JOIN

**As the name shows, JOIN means to combine something. In case of SQL, JOIN means "to combine two or more tables". The SQL JOIN clause takes records from two or more tables in a database and combines it together.**

# Why SQL JOIN is used?

* If you want to access more than one table through a select statement.

* If you want to combine two or more table then SQL JOIN statement is used .it combines rows of that tables in one table and one can retrieve the information by a SELECT statement.

* The joining of two or more tables is based on common field between them.

* SQL INNER JOIN also known as simple join is the most common type of join.

## INNER JOIN

**Staff Table**

	|  ID     | Staff_NAME | AGE     |  SALARY  |
	|		  |			   |         |   
	|	1	  |	  ARYAN	   |   22    |  18000   |
	|	2	  |	  SUSHIL   |   32    |  20000   |
	|	3	  |	  MONTY	   |   25    |  22000   |
	|	4	  |	  AMIT	   |   20    |  12000   |
	
**Payment table**

	|PaymentID |    DATE    | Staff_ID| AMOUNT  |
	|		   | 			|         |   
	|	101	   | 30/12/2009	|   1     |  3000   |
	|	102	   | 30/12/2009 |   3     |  2500   |
	|	103	   | 30/12/2009	|   4     |  3500   |


**INNER JOIN Query Example**
```
{
    SELECT Staff_ID, Staff_NAME, Staff_AGE, AMOUNT   
    FROM STAFF s, PAYMENT p  
    WHERE s.ID =p.STAFF_ID;  
}
```

**This will produce the result like this:**

	|  ID     | Staff_NAME | AGE     |  SALARY  |
	|		  |			   |         |   
	|	3	  |	  MONTY	   |   25    |  2500   |
	|	1	  |	  ARYAN	   |   22    |  3000   |
	|	4	  |	  AMIT	   |   20    |  3500   |
	|	1	  |	  ARYAN	   |   22    |  3000   |    


# Some other example of JOINS with syntax

## LEFT JOIN 

Returns all rows from the left table and the matching rows from the right table based on the join condition. If there is no match, NULL values are returned for the columns of the right table.

**Example**
```
{
    SELECT *
    FROM table1
    LEFT JOIN table2 ON table1.column = table2.column;  
}
```

## RIGHT JOIN 

Returns all rows from the right table and the matching rows from the left table based on the join condition. If there is no match, NULL values are returned for the columns of the left table.

**Example**
```
{
    SELECT *
    FROM table1
    RIGHT JOIN table2 ON table1.column = table2.column;  
}
```

## FULL JOIN or FULL OUTER JOIN

Returns all rows from both tables, matching the rows where the join condition is met. If there is no match, NULL values are returned for the columns of the non-matching table.

**Example**
```
{
    SELECT *
    FROM table1
    FULL JOIN table2 ON table1.column = table2.column;  
}
```

## CROSS JOIN

Returns the Cartesian product of both tables, meaning it combines each row from the first table with every row from the second table. It does not require a join condition.

**Example**
```
{
    SELECT *
    FROM table1
    CROSS JOIN table2;  
}
```

# Aggregate

**In SQL, aggregate functions are used to perform calculations on a set of rows and return a single result. These functions summarize or aggregate data within a column or across multiple columns. Here are some commonly used aggregate functions:**

### COUNT()

COUNT function is used to Count the number of rows in a database table. It can work on both numeric and non-numeric data types.
It uses the COUNT(*) that returns the count of all the rows in a specified table. COUNT(*) considers duplicate and Null.

**Example**
```
{
    SELECT COUNT(column_name)
    FROM table_name
    WHERE condition;
  
}
```

### SUM()

Sum function is used to calculate the sum of all selected columns. It works on numeric fields only.

**Example**
```
{
    SELECT SUM(column_name)
    FROM table_name
    WHERE condition;  
}
```

### AVG()

The AVG function is used to calculate the average value of the numeric type. AVG function returns the average of all non-Null values.

**Example**
```
{
    SELECT SUM(column_name)
    FROM table_name
    WHERE condition;  
}
```

### MIN()

MIN function is used to find the minimum value of a certain column. This function determines the smallest value of all selected values of a column.

**Example**
```
{
    SELECT MIN(column_name)
    FROM table_name
    WHERE condition;
  
}
```

### MAX()

MAX function is used to find the maximum value of a certain column. This function determines the largest value of all selected values of a column.

**Example**
```
{
    SELECT MAX(column_name)
    FROM table_name
    WHERE condition;
  
}
```

### GROUP BY()

Groups the rows based on one or more columns and performs aggregate calculations within each group.

**Example**
```
{
    SELECT column1, aggregate_function(column2)
    FROM table_name
    GROUP BY column1;

  
}
```


# References
<li> [W3school](https://www.w3schools.com/sql/),
<li> [TutorialsPoint](https://www.tutorialspoint.com/sql/index.htm),
<li> [Javatutorialspoint](https://www.tutorialspoint.com/sql/sql-using-joins.htm)