# Population Density Difference

**Problem:** [Population Density Difference](https://www.hackerrank.com/challenges/population-density-difference/problem)

## Intuition

Find the largest and smallest city populations, then subtract the minimum from the maximum to get the difference.

## Solution

```sql
SELECT MAX(population) - MIN(population)
FROM city;
```
