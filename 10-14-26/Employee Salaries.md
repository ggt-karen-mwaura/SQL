# Employee Salaries

**Link:** [Hackerrank - Employee Salaries](https://www.hackerrank.com/challenges/salary-of-employees/copy-from/485202376)

## Intuition
We need to find employees whose monthly salary is greater than 2000 and whose number of months working is less than 10. The result should be sorted by employee ID in ascending order so the output remains organized and easy to read.

## Solution
```sql
SELECT name
FROM Employee
WHERE salary > 2000
AND months < 10
ORDER BY employee_id ASC;
```
