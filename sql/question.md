1. Empty neighborhoods 

User table:  

columns | type 
------- | -------
id      | int 
name    | varchar 
neighborhoods | int 
created_at | datetime 

neighborhoods table:  

columns | type 
--------| -------
id      | int 
name    | varchar 
city_id | int 

Write a query that returns all of the neighborhoods that have 0 users. 

2. Distance traveled 

user table: 

columns | type 
--------| ------- 
id      |  int 
name    |  string 


rides table: 

columns | type 
--------| --------
id      | int 
passenger_user_id | int 
distance | float 

write a query to report the distance travelled by each user in descending order. 


3. employee salaries 

employees table: 

columns | types 
--------| -------
id      | int 
first_name | varchar 
last_name  | varchar 
salary     | int 
department_id | int 

departments table:

columns | types 
--------|--------
id      | int 
name    | varchar 

select top 3 departments with at least ten employees and rank them according to the percentage of their employees making over 100k in salary. 

4. Download facts 

user_dimension table: 

columns | types 
--------| -------
id      | int 
account_id | int 

account_dimension table: 

columns | types 
--------| -------
account_id      | int 
paying_customer | boolean 

download_facts table:

columns | types 
--------| -------
user_id | int 
date    | int 
downloads | int 

find the average numbers of downloads for free vs paying customers broken out by date. 

5. search ratings 

columns | types 
--------| -------
id      | int 
