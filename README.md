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
