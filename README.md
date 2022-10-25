# Day3-Lab1-SQL

1 ** Create a table "DS_bootcamp" containing three fields (trainee ID, trainee name, trainee university) and make the trainee ID the primary key

CREATE TABLE DS_bootcamp (
  trainee_ID int NOT NULL,
  trainee_name varchar(255),
  trainee_university varchar (255),
  PRIMARY KEY (trainee_ID)
  );
#===============================================================================================================================================
2 ** Insert at least 2 records into the DB_ Bootcamp table.

INSERT INTO DS_bootcamp
VALUES (1,'MAHA','KSU'),(2,'SARA', 'PNU')

#===============================================================================================================================================
3 ** Write a statement that will select the Country column from the Customers table.

SELECT country FROM Customers;

#===============================================================================================================================================
4 ** Select all the different values from the Country column in the Customers table.

SELECT DISTINCT country FROM Customers;

#===============================================================================================================================================
5 ** Write an SQL query to return only customers whose last name begins with R.

SELECT * FROM Customers
WHERE last_name LIKE 'R%';

#===============================================================================================================================================
6 ** List the number of customers in each country.

SELECT COUNT(customer_id),country
FROM Customers
GROUP BY country;

#===============================================================================================================================================
7 ** Select all records from the Customers table, sort the result alphabetically by the column first name.

SELECT * FROM Customers
ORDER BY  first_name ASC;

#===============================================================================================================================================
8 ** Select all records from the Customers table, sort the result reversed alphabetically by the column last name.

SELECT * FROM Customers
ORDER BY  last_name DESC;

#===============================================================================================================================================
9 ** Select all records where the item column has the value 'Mouse' and the amount column has the value 300.

SELECT * FROM Orders
WHERE item= 'Mouse' AND amount= 300;

#===============================================================================================================================================
10 ** Use the NOT keyword to select all records where status is NOT "Delivered".

SELECT * FROM Shippings
WHERE status is NOT 'Delivered';

#===============================================================================================================================================
11 ** Select all records where the country column has the value 'USA' or 'UAE'.

SELECT * FROM Customers
WHERE country = 'USA' OR country = 'UAE';

#===============================================================================================================================================
12 ** Select all records where the age column has the value 22 in customers table.

SELECT * FROM Customers
WHERE age = 22;

#===============================================================================================================================================
13 ** Use INNER to return the requested items with customers id.

SELECT Orders.item, Customers.customer_id
FROM Orders
INNER JOIN Customers ON Orders.Customer_ID = Customers.Customer_ID;

#===============================================================================================================================================
14 ** Choose the correct JOIN clause to select all records from the two tables where there is a match in both tables.

SELECT * FROM Customers
INNER JOIN Orders ON Customers.customer_id = Orders.customer_id;

#===============================================================================================================================================
15 ** Use the MIN function to select the record with the smallest value of the amount column from Orders table.

SELECT MIN(amount)
FROM Orders;

#===============================================================================================================================================
