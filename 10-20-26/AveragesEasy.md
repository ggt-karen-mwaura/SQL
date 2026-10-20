# Revising Aggregations - Averages

**Problem:** [Revising Aggregations - Averages](https://www.hackerrank.com/challenges/revising-aggregations-the-average-function/problem)

## Intuition

Filter the cities to California before averaging their populations. The `WHERE` clause ensures that cities in other districts do not affect the result.

## Solution

```sql
SELECT AVG(population)
FROM city
WHERE district = 'California';
```
