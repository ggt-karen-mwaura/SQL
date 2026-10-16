# Weather Observation Station 3

**Problem:** [Weather Observation Station 3](https://www.hackerrank.com/challenges/weather-observation-station-3/problem)

## Intuition

Keep only rows with an even station ID and use `DISTINCT` so each city appears once.

## Solution

```sql
SELECT DISTINCT city
FROM station
WHERE id %2 = 0;
```
