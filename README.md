	•	Create a table "DS_bootcamp" containing three fields (trainee ID, trainee name, trainee university) and make the trainee ID the primary key
        CREATE TABLE DS_bootcamp (
       trainee_ID int PRIMARY KEY,
        trainee_name varchar(50),
       trainee_university text
 
      );

	•	Insert at least 2 records into the DB_ Bootcamp table.
        INSERT INTO DS_bootcamp(trainee_ID, trainee_name, trainee_university)
        VALUES
       (1, 'Asma','KAUST'),
       (2, 'Lili','KAUST');


	•	Write a statement that will select the Country column from the Customers table.
	  Select country from Customers;



	•	Select all the different values from the Country column in the Customers table.
		Select distinct Country from Customers;

	•	Write an SQL query to return only customers whose last name begins with R.
	  Select last_name from Customers where last_name like 'R%';

	•	List the number of customers in each country.
	select count(customer_id), country
		from Customers
	  group by country;



	•	Select all records from the Customers table, sort the result alphabetically by the column first name.
	 select * from Customers
           Order by  first_name ASC;


	•	Select all records from the Customers table, sort the result reversed alphabetically by the column last name.
		 select * from Customers
		Order by  LAST_name DESC;

	•	Select all records where the item column has the value 'Mouse' and the amount column has the value 300.
		select * from Orders
		where item = 'Mouse' and amount ='300';



	•	Use the NOT keyword to select all records where status is NOT "Delivered".
		select * from Shippings
		where not status  ='Delivered';

	•	Select all records where the country column has the value 'USA' or 'UAE'.
		select * from Customers
		where country = 'USA' or country ='UAE';

	•	Select all records where the age column has the value 22 in customers table.
		select * from Customers
		where age = '22';

	•	Use INNER to return the requested items with customers id.
	   select * 
         from Customers
		inner join Orders on Customers.customer_id= Orders.customer_id;

	•	Choose the correct JOIN clause to select all records from the two tables where there is a match in both tables.
           select * 
           from Customers
		inner join Orders on Customers.customer_id= Orders.customer_id;

	•	Use the MIN function to select the record with the smallest value of the amount column from Orders table.
		select min (amount)
           from Orders;
