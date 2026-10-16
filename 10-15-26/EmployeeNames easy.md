# Employee Names

**Problem:** [Employee Names](https://www.hackerrank.com/challenges/name-of-employees/problem)

## Intuition

Select the `name` column from every employee record, then sort the names alphabetically.

## Solution

```sql
SELECT name
FROM Employee
ORDER BY name ASC;
```