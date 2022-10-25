# Day3-Lab1-SQL

- Create a table "DS_bootcamp" containing three fields (trainee ID, trainee name, trainee university) and make the trainee ID the primary key
Ans: 
CREATE TABLE bootcamp.DS_bootcamp (
    traineeID int NOT NULL PRIMARY KEY,
    traineeName varchar(255),
    traineeUniversity varchar(255)
);

- Insert at least 2 records into the DB_ Bootcamp table.
Ans:
INSERT INTO DS_bootcamp (`traineeID`, `traineeName`, `traineeUniversity`) 
VALUES ('1', 'Rawabe', 'Hail Uni'),
('2', 'Rahaf', 'Abha Uni');

- Write a statement that will select the Country column from the Customers table.
Ans:
SELECT Country FROM Customers;

- Select all the different values from the Country column in the Customers table.
Ans:
SELECT DISTINCT Country FROM Customers;

- Write an SQL query to return only customers whose last name begins with R.
Ans:
SELECT * FROM Customers WHERE last_name LIKE 'R%';

- List the number of customers in each country.
Ans:
SELECT count(customer_id) as custmers_count, country 
FROM Customers
Group BY country;

- Select all records from the Customers table, sort the result alphabetically by the column first name.
Ans:
SELECT * FROM Customers
ORDER BY first_name;

- Select all records from the Customers table, sort the result reversed alphabetically by the column last name.
Ans:
SELECT * FROM Customers
ORDER BY last_name DESC;

- Select all records where the item column has the value 'Mouse' and the amount column has the value 300.
Ans:
SELECT * FROM Orders
WHERE item = 'Mouse' AND amount = 300;

- Use the NOT keyword to select all records where status is NOT "Delivered".
Ans:
SELECT * FROM Shippings
WHERE NOT status = 'Delivered';

- Select all records where the country column has the value 'USA' or 'UAE'.
Ans:
SELECT * FROM Customers
WHERE country = 'USA' or country = 'UAE';

- Select all records where the age column has the value 22 in customers table.
Ans:
SELECT * FROM Customers
WHERE age = 22;

- Use INNER to return the requested items with customers id.
Ans:
SELECT Orders.item, Customers.customer_id
FROM Orders
INNER JOIN Customers
ON Orders.customer_id = Customers.customer_id;

- Choose the correct `JOIN` clause to select all records from the two tables where there is a match in both tables.
Ans:
SELECT Orders.*, Customers.*
FROM Orders
INNER JOIN Customers
ON Orders.customer_id = Customers.customer_id;

- Use the MIN function to select the record with the smallest value of the amount column from Orders table.
Ans:
SELECT min(amount) as smallest_amount 
FROM Orders;

