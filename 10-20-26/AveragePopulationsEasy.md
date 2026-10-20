# Average Population

**Problem:** [Average Population](https://www.hackerrank.com/challenges/average-population/problem)

## Intuition

Take the average of the population values across all cities. Round the result to the nearest integer, as required by the challenge.

## Solution

```sql
SELECT ROUND(AVG(population))
FROM city;
```
