# Day3-Lab1-SQL

- Create a table "DS_bootcamp" containing three fields (trainee ID, trainee name, trainee university) and make the trainee ID the primary key

Answer: CREATE TABLE DS_bootcamp (
    trainee_ID INTEGER PRIMARY KEY,
    trainee_name VARCHAR(255),
    trainee_university VARCHAR(255)
)

- Insert at least 2 records into the DB_ Bootcamp table.

Answer: INSERT INTO DS_bootcamp VALUES (1, 'yasser', 'KSU');

INSERT INTO DS_bootcamp VALUES (199,' cactusy', 'Cactusity');


- Write a statement that will select the Country column from the Customers table.

Answer: SELECT country FROM Customers;  

- Select all the different values from the Country column in the Customers table.

Answer: SELECT DISTINCT country FROM Customers;

- Write an SQL query to return only customers whose last name begins with R.

Answer: SELECT * FROM Customers WHERE last_name LIKE 'R%';

- List the number of customers in each country.

Answer: SELECT COUNT(customer_id) FROM Customers GROUP BY country;

- Select all records from the Customers table, sort the result alphabetically by the column first name.

Answer: SELECT * FROM Customers ORDER BY first_name ASC;

- Select all records from the Customers table, sort the result reversed alphabetically by the column last name.

Answer: SELECT * FROM Customers ORDER BY last_name DESC;

- Select all records where the item column has the value 'Mouse' and the amount column has the value 300.

Answer: SELECT * FROM Orders WHERE item LIKE 'Mouse' AND amount = 300;


- Use the NOT keyword to select all records where status is NOT "Delivered".

Answer: SELECT * FROM Shippings WHERE NOT status = 'Delivered';

- Select all records where the country column has the value 'USA' or 'UAE'.

Answer: SELECT * FROM Customers WHERE country IN ( 'USA', 'UAE' );

- Select all records where the age column has the value 22 in customers table.

Answer: SELECT * FROM Customers WHERE age = 22;

- Use INNER to return the requested items with customers id.

Answer: SELECT Orders.customer_id,item FROM Orders
INNER JOIN Customers ON Customers.customer_id = Orders.customer_id

- Choose the correct `JOIN` clause to select all records from the two tables where there is a match in both tables.

Answer: SELECT * FROM Orders
JOIN Customers WHERE Customers.customer_id = Orders.customer_id


- Use the MIN function to select the record with the smallest value of the amount column from Orders table.

Answer: SELECT * FROM Orders
WHERE amount IN ( SELECT MIN(amount) FROM Orders) 