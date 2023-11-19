![image](https://github.com/sandvoxy/sql/assets/112099595/855c7e73-d12c-46c4-8503-d36a079d0411)
1757. Recyclable and Low Fat Products
Easy

Table: Products

+-------------+---------+
| Column Name | Type    |
+-------------+---------+
| product_id  | int     |
| low_fats    | enum    |
| recyclable  | enum    |
+-------------+---------+
product_id is the primary key (column with unique values) for this table.
low_fats is an ENUM (category) of type ('Y', 'N') where 'Y' means this product is low fat and 'N' means it is not.
recyclable is an ENUM (category) of types ('Y', 'N') where 'Y' means this product is recyclable and 'N' means it is not.
 
Write a solution to find the ids of products that are both low fat and recyclable.

Return the result table in any order.
![image](https://github.com/sandvoxy/sql/assets/112099595/ab2950fa-90c1-4a32-90b6-b770a7d819e4)


The result format is in the following example.

SOLUTION

SELECT product_id
FROM Products
WHERE low_fats = 'Y'
AND recyclable = 'Y'; 

