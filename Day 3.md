1667. Fix Names in a Table
https://leetcode.com/problems/fix-names-in-a-table/

Solution:

SELECT user_id,
CONCAT(UPPER(SUBSTRING(name,1,1)),LOWER(SUBSTRING(name,2))) AS name 
FROM Users
ORDER BY user_id

1484. Group Sold Products By The Date
https://leetcode.com/problems/group-sold-products-by-the-date/

Solution:

SELECT sell_date,COUNT(product) AS num_sold,
STRING_AGG(product, ',') WITHIN GROUP(ORDER BY PRODUCT ASC) AS products
FROM (SELECT DISTINCT sell_date,product FROM Activities)TEMP
GROUP BY sell_date
ORDER BY sell_date

1527. Patients With a Condition
https://leetcode.com/problems/patients-with-a-condition/

Solution 1:

SELECT * FROM Patients
WHERE conditions LIKE ('% DIAB1%') OR conditions LIKE ('DIAB1%')
