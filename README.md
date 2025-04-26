# LeetCodeSQL50
My Solutions to LeetCode Study Plan  'SQL 50'  

## Easy -> SELECT

### 1757. Recyclable and Low Fat Products

    SELECT product_id FROM products WHERE low_fats = 'Y' AND recyclable = 'Y';

### 584. Find Customer Referee

    SELECT name FROM Customer WHERE referee_id <> 2 OR referee_id is null 

### 595. Big Countries
    SELECT name, population, area FROM WORLD WHERE area >= 3000000 OR population >= 25000000;

### 1148. Article Views I
    SELECT DISTINCT author_id as id FROM Views WHERE author_id = viewer_id ORDER BY id ASC;

### 1683. Invalid Tweets
    SELECT tweet_id FROM Tweets WHERE  LENGTH(content) > 15;
## Easy -> JOIN

### 1378. Replace Employee ID With The Unique Identifier
    SELECT  EmployeeUNI.unique_id, Employees.name from Employees LEFT JOIN EmployeeUNI ON Employees.id = EmployeeUNI.id;

### 1068. Product Sales Analysis I
    SELECT Product.product_name, year, price FROM Sales JOIN Product ON Product.product_id = Sales.product_id;

### 1581. Customer Who Visited but Did Not Make Any Transactions
        SELECT customer_id, COUNT(visit_id) as count_no_trans 
        FROM Visits
        WHERE  Visits.visit_id NOT IN (
            SELECT visit_id
            FROM Transactions
        )
        GROUP BY Visits.customer_id; 

### 197. Rising Temperature
    SELECT a.id FROM Weather as a
    JOIN Weather as b
    ON a.recordDate = DATE_ADD(b.recordDate, INTERVAL 1 day)
    where a.temperature > b.temperature;
