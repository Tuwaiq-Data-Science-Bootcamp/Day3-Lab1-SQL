# Day3-Lab1-SQL

### Create a table "DS_bootcamp" containing three fields (trainee ID, trainee name, trainee university) and make the trainee ID the primary key

``` SQL

CREATE TABLE DS_bootcamp (
trainee_ID int NOT NULL,
trainee_name varchar(255),
trainee_university varchar(255),
PRIMARY KEY (trainee_ID)
);

```
### Insert at least 2 records into the DB_ Bootcamp table.

``` SQL

INSERT INTO DS_bootcamp VALUES
(1,"Ghadah","KSU"),
(2,"Haifa","PNU"),
(3,"Walla","MPU"),
(4,"Nada","PSU");

```

### Write a statement that will select the Country column from the Customers table.
``` SQL
SELECT Country FROM Customers;
```

### Select all the different values from the Country column in the Customers table.
``` SQL
SELECT DISTINCT(Country) FROM Customers;

```
### Write an SQL query to return only customers whose last name begins with R.
``` SQL
SELECT * FROM Customers WHERE last_name LIKE 'R%';

```
### List the number of customers in each country.
``` SQL
SELECT Count(*), Country FROM Customers GROUP BY Country;
```
### Select all records from the Customers table, sort the result alphabetically by the column first name.
``` SQL
SELECT * FROM Customers ORDER BY first_name;
```
### Select all records from the Customers table, sort the result reversed alphabetically by the column last name.
``` SQL
SELECT * FROM Customers ORDER BY first_name DESC;

```
### Select all records where the item column has the value 'Mouse' and the amount column has the value 300.
``` SQL
SELECT * FROM Orders WHERE item LIKE 'Mouse' AND amount = 300;

```
### Use the NOT keyword to select all records where status is NOT "Delivered".
``` SQL
SELECT * FROM Shippings WHERE status NOT LIKE 'Delivered';
```
### Select all records where the country column has the value 'USA' or 'UAE'.
``` SQL
SELECT * FROM Customers WHERE country IN ('USA','UAE');

```
### Select all records where the age column has the value 22 in customers table.
``` SQL
SELECT * FROM Customers WHERE age = 22;

```
### Use INNER to return the requested items with customers id.
``` SQL
SELECT Orders.item, Customers.customer_id FROM Orders INNER JOIN Customers ON  Customers.customer_id == Orders.customer_id;

```
### Choose the correct `JOIN` clause to select all records from the two tables where there is a match in both tables.
``` SQL
SELECT * FROM Orders INNER JOIN Customers ON  Customers.customer_id == Orders.customer_id;
```
### Use the MIN function to select the record with the smallest value of the amount column from Orders table.
``` SQL
SELECT *, MIN(amount) FROM Orders;
```