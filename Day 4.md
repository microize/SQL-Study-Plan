1965. Employees With Missing Information
https://leetcode.com/problems/employees-with-missing-information/

(
SELECT employee_id FROM Employees
EXCEPT
SELECT employee_id FROM Salaries
)
UNION
(
SELECT employee_id FROM Salaries
EXCEPT
SELECT employee_id FROM Employees
)


176. Second Highest Salary
https://leetcode.com/problems/second-highest-salary/

SELECT MAX(salary) AS SecondHighestSalary
FROM (
SELECT DISTINCT salary FROM Employee
ORDER BY salary DESC
OFFSET 1 ROWS
FETCH NEXT 1 ROWS ONLY
) TEMP
