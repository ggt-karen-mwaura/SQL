# Higher Than 75 Marks

**Problem:** [Higher Than 75 Marks](https://www.hackerrank.com/challenges/more-than-75-marks/problem)

## Intuition

Filter students to those scoring above 75. Sort by the final three characters of each name, then by ID to break ties.

## Solution

```sql
SELECT name
FROM students
WHERE marks > 75
ORDER BY RIGHT(name, 3), ID;
```
