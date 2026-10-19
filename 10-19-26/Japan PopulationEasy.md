# Japan Population

**Problem:** [Japan Population](https://www.hackerrank.com/challenges/japan-population/problem)

## Intuition

Filter the `city` table to rows whose country code is Japan (`JPN`), then add their population values to get the country's total population.

## Solution

```sql
SELECT SUM(population)
FROM city
WHERE countrycode = 'JPN';
```