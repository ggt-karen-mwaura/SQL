# Top Earners

**Problem:** [Top Earners](https://www.hackerrank.com/challenges/earnings-of-employees/problem)

## Intuition

An employee's total earnings are their salary multiplied by the number of months worked. Find the maximum of that value, then count the employees whose earnings equal that maximum.

## Solution

```sql
SELECT
    salary * months AS max_earnings,
    COUNT(employee_id)
FROM Employee
WHERE salary * months = (
    SELECT MAX(salary * months)
    FROM Employee
)
GROUP BY salary * months;
```