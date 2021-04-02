# 1. Understanding SQL 

Database: a container that stores organized data. 

Table: a structured list of a specific type. 

# 2 Retrieving Data 

The **SELECT** statement 

Select individual column 

```sql
SELECT name 
FROM table; 
```
Select multiple columns

```sql
SELECT name1, name2
FROM table; 
```
Select all columns

```sql
SELECT *
FROM table; 
```
Select distinct rows 

```sql
SELECT DISTINCT name 
FROM table; 
# use distinct
```

Select limited rows

```sql
SELECT TOP 5 name  
FROM table; -- Microsoft SQL server, check for different DBMS. 
/*SELECT name  
FROM table
LIMIT 5;*/ -- MySQL  
```

# 1 constraints 

Rules that govern how database data is inserted and manipulated. 

# 2 Primary Key 

# 3 Foreign Key 

# 4 