# LeetCodeSQL50
My Solutions to LeetCode Study Plan  'SQL 50'  

### 1757. Recyclable and Low Fat Products

    SELECT product_id FROM products WHERE low_fats = 'Y' AND recyclable = 'Y';

### 584. Find Customer Referee

    SELECT name FROM Customer WHERE referee_id <> 2 OR referee_id is null 

### 595. Big Countries
    SELECT name, population, area FROM WORLD WHERE area >= 3000000 OR population >= 25000000;
