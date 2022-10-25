create table DS_bootcamp (trainee_ID not null , trainee_name, trainee_university, PRIMARY KEY (trainee_ID) );


insert into DS_bootcamp (trainee_ID, trainee_name, trainee_university) values (1,'khalid', 'imam mohammed');

insert into DS_bootcamp (trainee_ID, trainee_name, trainee_university) values (2,'faisal', 'king saud');

select Country from Customers ; 

select distinct Country from Customers ; 

select * from customers where last_name like "R%";

SELECT COUNT(Customer_id),Country FROM Customers
GROUP BY Country
ORDER BY COUNT(Customer_id);

SELECT * FROM Customers ORDER BY first_name ASC;

SELECT * FROM Customers ORDER BY last_name DESC;

Select * from orders 
where item = "Mouse" and amount = 300;


Select * from Shippings                    
where  not status="Delivered";



select * from customers where country = 'USA' OR country ='UAE';


select * from customers where AGE = 22 ;

select MIN (amount) from orders ; 



SELECT *	FROM Orders	INNER JOIN Customers
ON Orders.customer_id=Customers.customer_id;


SELECT *	FROM Orders	INNER JOIN Customers
ON Orders.item=Customers.customer_id;






 
