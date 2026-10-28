# The Blunder

**Problem:** [The Blunder](https://www.hackerrank.com/challenges/the-blunder/problem)

## Intuition

The incorrect average is calculated by removing every zero from each salary before converting it back to a number. Subtract this incorrect average from the true average, then use `CEIL` to round the error up to the next integer as requested.

## Solution

```sql
SELECT CEIL(AVG(Salary) - AVG(CAST(REPLACE(Salary, '0', '') AS UNSIGNED)))
FROM EMPLOYEES;
```