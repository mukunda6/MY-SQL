-------------------------------------------------------------------------------

1. What is MySQL and what are its key features?

Answer

MySQL is an open-source Relational Database Management System (RDBMS) used to store, manage, and retrieve data using SQL (Structured Query Language).

It stores data in the form of:
• Tables
• Rows
• Columns

Key Features
• Open Source
• High Performance
• Scalability
• Security and User Authentication
• ACID Compliance
• Cross Platform Support
• Indexing Support
• Backup and Recovery

Example

SELECT * FROM students;

-------------------------------------------------------------------------------
-------------------------------------------------------------------------------

2. What is the default port for MySQL?

Answer

The default port number for MySQL is:

3306

MySQL server listens on port 3306 by default for client connections.

Example

mysql -h localhost -P 3306 -u root -p

Where:
• -h → Hostname
• -P → Port Number
• -u → Username
• -p → Password

Important Point

If multiple MySQL instances are running, different port numbers can also be configured manually.

-------------------------------------------------------------------------------
-------------------------------------------------------------------------------

3. Explain the difference between SQL and MySQL.

Answer

SQL and MySQL are different but related concepts.

SQL
• SQL stands for Structured Query Language
• It is a standard language used to interact with databases
• Used to perform operations like SELECT, INSERT, UPDATE, and DELETE
• SQL is a language, not software

MySQL
• MySQL is an open-source Relational Database Management System (RDBMS)
• It is software used to store and manage databases
• MySQL uses SQL language to perform database operations
• Developed and maintained by Oracle Corporation

Key Difference

• SQL is a language
• MySQL is database software that uses SQL

Example

SELECT * FROM employees;

-------------------------------------------------------------------------------
-------------------------------------------------------------------------------

4. How do you see all the databases available on the MySQL server?

Answer

To display all databases available on the MySQL server, use the following command:

SHOW DATABASES;

This command lists all databases that the current user has permission to view.

Example Output

information_schema
mysql
performance_schema
company_db
student_db

Important Point

• You must have proper access permissions to view databases.
• System databases are also displayed by default.

-------------------------------------------------------------------------------
-------------------------------------------------------------------------------

5. What command is used to select a database?

Answer

The USE command is used to select a database in MySQL.

Syntax

USE database_name;

Example

USE company_db;

After selecting the database, all SQL operations are performed on that database until another database is selected.

Important Point

• The database must already exist before using the USE command.
• Only one database can be selected at a time in a session.

-------------------------------------------------------------------------------
-------------------------------------------------------------------------------

6. How do you view the structure of a table?

Answer

To view the structure of a table in MySQL, use the DESCRIBE or DESC command.

Syntax

DESCRIBE table_name;

or

DESC table_name;

Example

DESC employees;

This command shows:
• Column names
• Data types
• NULL values
• Key information
• Default values
• Extra properties

Example Output

id          INT         PRIMARY KEY
name        VARCHAR(50)
salary      INT

Important Point

• DESCRIBE and DESC both perform the same function.
• It is useful for understanding table schema and column details.

-------------------------------------------------------------------------------
-------------------------------------------------------------------------------

7. What is a Primary Key?

Answer

A Primary Key is a column or set of columns used to uniquely identify each record in a table.

Features of Primary Key
• Values must be unique
• Cannot contain NULL values
• Each table can have only one Primary Key
• Helps maintain data integrity

Example

CREATE TABLE students (
    id INT PRIMARY KEY,
    name VARCHAR(50),
    marks INT
);

In this example:
• id is the Primary Key
• Each student will have a unique id

Real-Time Example

Consider an Aadhaar Number system.

• Every citizen has a unique Aadhaar number
• No two people can have the same Aadhaar number
• It uniquely identifies each person

Similarly, in a school database:
• Student ID uniquely identifies each student

Example Table

Student_ID      Name         Marks
101             Rahul        85
102             Priya        92
103             Arjun        78

Here:
• Student_ID is the Primary Key
• Each value is unique

Important Point

• Primary Keys improve data organization and relationships between tables.
• Primary Keys are often used with Foreign Keys.

-------------------------------------------------------------------------------
-------------------------------------------------------------------------------

8. What is a Foreign Key?

Answer

A Foreign Key is a column or set of columns in one table that creates a relationship with the Primary Key of another table.

It is used to maintain referential integrity between tables.

Features of Foreign Key
• Creates relationships between tables
• Prevents invalid data entry
• References the Primary Key of another table
• Allows duplicate values
• Can contain NULL values

Example

CREATE TABLE customers (
    customer_id INT PRIMARY KEY,
    customer_name VARCHAR(50)
);

CREATE TABLE orders (
    order_id INT PRIMARY KEY,
    customer_id INT,
    FOREIGN KEY (customer_id)
    REFERENCES customers(customer_id)
);

In this example:
• customer_id in customers table is the Primary Key
• customer_id in orders table is the Foreign Key

Real-Time Example

Consider an E-commerce Application.

Customers Table

Customer_ID      Customer_Name
101              Rahul
102              Priya

Orders Table

Order_ID         Customer_ID
5001             101
5002             102

Here:
• Customer_ID in Orders table refers to Customer_ID in Customers table
• An order cannot exist without a valid customer

This relationship helps connect customers with their orders.

Important Point

• Foreign Keys help maintain consistency between related tables.
• They are mainly used in relational databases to establish table relationships.

-------------------------------------------------------------------------------
-------------------------------------------------------------------------------

9. Explain the CHAR vs. VARCHAR data types.

Answer

CHAR and VARCHAR are data types used to store character strings in MySQL.

CHAR
• Fixed-length data type
• Allocates full specified memory even if data is smaller
• Faster in performance for fixed-size data
• Wastes memory if data length varies

VARCHAR
• Variable-length data type
• Uses only required memory
• Saves storage space
• Slightly slower compared to CHAR

Example

name CHAR(10);
city VARCHAR(50);

Explanation
• CHAR(10) always stores 10 characters
• VARCHAR(50) stores only the actual entered characters

Real-Time Example

Consider storing Gender values:

• Male
• Female

Since the values are fixed and small, CHAR is better.

Example

gender CHAR(6);

Now consider storing Email Addresses:

• Different users have different email lengths

VARCHAR is better because it saves memory.

Example

email VARCHAR(100);

Key Differences

CHAR
• Fixed Length
• Faster
• Wastes Space

VARCHAR
• Variable Length
• Memory Efficient
• Flexible Storage

Important Point

• Use CHAR for fixed-size values like Gender, Country Code, PIN.
• Use VARCHAR for variable-length values like Names, Emails, Addresses.

-------------------------------------------------------------------------------
-------------------------------------------------------------------------------

10. What is the difference between INT and BIGINT?

Answer

INT and BIGINT are numeric data types used to store integer values in MySQL.

INT
• Uses 4 bytes of storage
• Stores smaller integer values
• Range:
  -2147483648 to 2147483647

BIGINT
• Uses 8 bytes of storage
• Stores very large integer values
• Range:
  -9223372036854775808 to 9223372036854775807

Example

age INT;
population BIGINT;

Real-Time Example

INT Example
• Storing student marks
• Employee age
• Product quantity

Example

marks INT;

BIGINT Example
• Storing population data
• Bank transaction IDs
• Large application user counts

Example

youtube_views BIGINT;

Explanation

• INT is suitable for normal-sized numbers.
• BIGINT is used when the value can become extremely large.

Key Differences

INT
• 4 Bytes
• Smaller Range
• Less Storage

BIGINT
• 8 Bytes
• Larger Range
• More Storage

Important Point

• Use INT for regular numeric values.
• Use BIGINT when handling huge numbers to avoid overflow issues.

-------------------------------------------------------------------------------
-------------------------------------------------------------------------------

11. How do you create a table in MySQL?

Answer

In MySQL, the CREATE TABLE statement is used to create a new table in a database.

Syntax

CREATE TABLE table_name (
    column1 datatype,
    column2 datatype,
    column3 datatype
);

Example

CREATE TABLE employees (
    id INT PRIMARY KEY,
    name VARCHAR(50),
    salary INT,
    department VARCHAR(30)
);

In this example:
• employees → Table Name
• id, name, salary, department → Columns
• INT and VARCHAR → Data Types

Real-Time Example

Consider an Employee Management System.

A company needs to store employee details such as:
• Employee ID
• Employee Name
• Salary
• Department

For this, a table is created:

CREATE TABLE employees (
    employee_id INT PRIMARY KEY,
    employee_name VARCHAR(100),
    salary INT,
    department VARCHAR(50)
);

Sample Data

Employee_ID      Employee_Name      Department
101              Rahul              HR
102              Priya              IT
103              Arjun              Finance

Important Point

• A table must have unique column names.
• Proper data types should be selected for efficient storage.
• Primary Keys are commonly added while creating tables.

-------------------------------------------------------------------------------
-------------------------------------------------------------------------------

12. What is an Alias in MySQL?

Answer

An Alias in MySQL is a temporary name given to a column or a table to make the output more readable and understandable.

Aliases are created using the AS keyword.

Syntax

SELECT column_name AS alias_name
FROM table_name;

Example

SELECT name AS employee_name
FROM employees;

In this example:
• name is the original column name
• employee_name is the alias

The output will display employee_name instead of name.

Table Alias Example

SELECT e.name, e.salary
FROM employees AS e;

Here:
• e is the alias for employees table

Real-Time Example

Consider a company database where the column name is:

emp_salary

This may not look user-friendly in reports.

Using Alias:

SELECT emp_salary AS Monthly_Salary
FROM employees;

Output

Monthly_Salary
50000
65000
70000

This makes the report easier to understand.

Key Benefits of Alias

• Improves readability
• Makes column names user-friendly
• Useful in reports and dashboards
• Simplifies complex queries

Important Point

• Aliases are temporary and exist only during query execution.
• AS keyword is optional in MySQL.

Example Without AS

SELECT name employee_name
FROM employees;

-------------------------------------------------------------------------------
-------------------------------------------------------------------------------

13. How do you filter unique values in a query?

Answer

In MySQL, the DISTINCT keyword is used to filter unique values from a column.

It removes duplicate records from the query result.

Syntax

SELECT DISTINCT column_name
FROM table_name;

Example

SELECT DISTINCT department
FROM employees;

This query displays only unique department names.

Real-Time Example

Consider an Employee Table.

Employee_Name      Department
Rahul              IT
Priya              HR
Arjun              IT
Sneha              Finance
Kiran              HR

If we run:

SELECT DISTINCT department
FROM employees;

Output

IT
HR
Finance

Here:
• Duplicate department values are removed
• Only unique values are displayed

Using DISTINCT with Multiple Columns

Example

SELECT DISTINCT department, city
FROM employees;

This returns unique combinations of department and city.

Key Benefits

• Removes duplicate records
• Helps in data analysis
• Improves report clarity
• Useful for generating unique lists

Important Point

• DISTINCT works on complete selected values.
• It can be used with one or multiple columns.

-------------------------------------------------------------------------------
-------------------------------------------------------------------------------

14. What does the LIKE operator do?

Answer

The LIKE operator in MySQL is used for pattern matching in SQL queries.

It helps search for specific patterns in text data.

LIKE is commonly used with wildcard characters.

Wildcards Used in LIKE

• %  → Represents multiple characters
• _  → Represents a single character

Syntax

SELECT column_name
FROM table_name
WHERE column_name LIKE pattern;

Example 1

SELECT * FROM employees
WHERE name LIKE 'A%';

Explanation
• Finds names starting with the letter A

Example Output

Akhil
Ananya
Arjun

Example 2

SELECT * FROM employees
WHERE name LIKE '%n';

Explanation
• Finds names ending with the letter n

Example Output

Kiran
Mohan

Example 3

SELECT * FROM employees
WHERE name LIKE '_a%';

Explanation
• Second character must be 'a'

Real-Time Example

Consider an E-commerce Website.

A customer searches for products starting with "Sam".

Query

SELECT * FROM products
WHERE product_name LIKE 'Sam%';

Output

Samsung Galaxy S24
Samsung TV
Samsung Watch

This helps users search products quickly.

Key Benefits

• Used for searching text patterns
• Helpful in search functionality
• Improves filtering of records
• Supports flexible matching

Important Point

• LIKE is mainly used with VARCHAR or TEXT columns.
• Pattern matching is case-insensitive in many MySQL configurations.

-------------------------------------------------------------------------------
-------------------------------------------------------------------------------

15. What is the purpose of the LIMIT clause?

Answer

The LIMIT clause in MySQL is used to restrict the number of rows returned by a query.

It helps display only a specific number of records from a table.

Syntax

SELECT column_name
FROM table_name
LIMIT number;

Example

SELECT * FROM employees
LIMIT 5;

Explanation
• Returns only the first 5 rows from the employees table

Using LIMIT with OFFSET

Syntax

SELECT column_name
FROM table_name
LIMIT offset, count;

Example

SELECT * FROM employees
LIMIT 5, 5;

Explanation
• Skips the first 5 rows
• Displays the next 5 rows

Real-Time Example

Consider an E-commerce Website.

When a user opens a product page:
• Thousands of products may exist
• Showing all products at once reduces performance

Instead, only limited products are displayed.

Example

SELECT * FROM products
LIMIT 10;

This displays:
• Only the first 10 products on the page

This technique is commonly used in:
• Pagination
• Dashboards
• Search Results
• Reports

Key Benefits

• Improves query performance
• Reduces unnecessary data loading
• Helps implement pagination
• Makes output easier to read

Important Point

• LIMIT is mainly used with SELECT queries.
• Often combined with ORDER BY for accurate results.

Example

SELECT * FROM employees
ORDER BY salary DESC
LIMIT 3;

This returns the top 3 highest-paid employees.

-------------------------------------------------------------------------------
