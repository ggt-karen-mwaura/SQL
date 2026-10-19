# Revising Aggregations - The Sum Function

**Problem:** [Revising Aggregations - The Sum Function](https://www.hackerrank.com/challenges/revising-aggregations-sum/problem)

## Intuition

Filter the `city` table to California, then use `SUM` to aggregate the population of all matching cities.

## Solution

```sql
SELECT SUM(population)
FROM city
WHERE district = 'California';
```
