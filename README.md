# Day3-Lab1-SQL

- Create a table "DS_bootcamp" containing three fields (trainee ID, trainee name, trainee university) and make the trainee ID the primary key


CREATE TABLE DS_Bootcamp(  trainee_id int NOT NULL,
			   trainee_name varchar(255),
			   trainee_uni varchar(255),
			   PRIMARY KEY (trainee_id)) 
         
         
- Insert at least 2 records into the DB_ Bootcamp table.

INSERT INTO DS_Bootcamp
VALUES (1,'Meshari','Imam Muhammad Ibn Saud')

INSERT INTO DS_Bootcamp
VALUES (2,'Faisal','King Saud University')

INSERT INTO DS_Bootcamp
VALUES (3,'Faris','King Abdilaziz University')

- Write a statement that will select the Country column from the Customers table.

SELECT country FROM Customers

- Select all the different values from the Country column in the Customers table.

SELECT DISTINCT country FROM Customers

- Write an SQL query to return only customers whose last name begins with R.

SELECT  last_name FROM Customers
WHERE last_name LIKE 'R%'

- List the number of customers in each country.

SELECT country, count(country) FROM Customers
GROUP BY 1

- Select all records from the Customers table, sort the result alphabetically by the column first name.

SELECT * FROM Customers
ORDER BY first_name

- Select all records from the Customers table, sort the result reversed alphabetically by the column last name.

SELECT * FROM Customers
ORDER BY last_name DESC


- Select all records where the item column has the value 'Mouse' and the amount column has the value 300.

SELECT * FROM Orders
WHERE item = 'Mouse' AND amount = 300

- Use the NOT keyword to select all records where status is NOT "Delivered".

SELECT * FROM Shippings
WHERE status <> 'Delivered'


- Select all records where the country column has the value 'USA' or 'UAE'.

SELECT * FROM Customers
WHERE country = 'USA' OR country = 'UAE'


- Select all records where the age column has the value 22 in customers table.

SELECT * FROM Customers
WHERE age = 22

- Use INNER to return the requested items with customers id.

SELECT c.customer_id, c.first_name , c.last_name ,o.item
FROM Customers as c
JOIN Orders as o
ON c.customer_id = o.customer_id

- Choose the correct `JOIN` clause to select all records from the two tables where there is a match in both tables.

SELECT *
FROM Customers 
INNER JOIN Orders ON Customers.customer_id = Orders.customer_id

- Use the MIN function to select the record with the smallest value of the amount column from Orders table.

SELECT *, MIN(amount)
FROM Orders



