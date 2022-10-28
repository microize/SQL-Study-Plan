595. Big Countries
https://leetcode.com/problems/big-countries/

Solution 1:

SELECT name,population,area FROM World
WHERE population >= 25000000 OR area >= 3000000

Solution 2:

SELECT name,population,area FROM World
WHERE population >= 25000000 
UNION
SELECT name,population,area FROM World
WHERE area >= 3000000

************************************************
************************************************

1757. Recyclable and Low Fat Products
https://leetcode.com/problems/recyclable-and-low-fat-products/submissions/832066828/

Solution 1:

SELECT product_id FROM Products
WHERE low_fats = 'Y' AND recyclable = 'Y'

************************************************
************************************************

584. Find Customer Referee
https://leetcode.com/problems/find-customer-referee/

Solution 1:

SELECT name FROM Customer
WHERE referee_id <>2 OR referee_id IS NULL


************************************************
************************************************

183. Customers Who Never Order
https://leetcode.com/problems/customers-who-never-order/

Solution 1:

SELECT name as Customers
FROM Customers
WHERE id NOT IN (SELECT DISTINCT customerId FROM Orders)
