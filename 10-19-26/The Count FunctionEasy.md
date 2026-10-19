# Revising Aggregations - The Count Function

**Problem:** [Revising Aggregations - The Count Function](https://www.hackerrank.com/challenges/revising-aggregations-the-count-function/problem)

## Intuition

Count the names of cities whose population exceeds 100,000. The `WHERE` clause filters the rows before `COUNT` returns the number of matching names.

## Solution

```sql
SELECT COUNT(name)
FROM city
WHERE population > 100000;
```
