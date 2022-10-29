#1873. Calculate Special Bonus
https://leetcode.com/problems/calculate-special-bonus

Solution 1:

SELECT employee_id, 
CASE WHEN (employee_id%2) <> 0 AND name NOT LIKE 'M%' 
     THEN salary 
     ELSE 0 END AS bonus
FROM Employees
ORDER BY employee_id


*************************************************
*************************************************
627. Swap Salary
https://leetcode.com/problems/swap-salary/

Solution 1:

UPDATE salary
SET sex = CASE WHEN sex ='m' THEN 'f' ELSE 'm' END

*************************************************
*************************************************
196. Delete Duplicate Emails
https://leetcode.com/problems/delete-duplicate-emails/

Solution 1:

DELETE P1 FROM Person P1, Person P2
WHERE P1.email = P2.email
AND P1.id > P2.id
