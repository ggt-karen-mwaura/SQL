# Weather Observation Station 15

**Problem:** [Weather Observation Station 15](https://www.hackerrank.com/challenges/weather-observation-station-15/problem)

## Intuition

Find the greatest latitude below the upper bound, then use that latitude to select its corresponding longitude. Round the longitude to four decimal places.

## Solution

```sql
SELECT ROUND(LONG_W, 4)
FROM station
WHERE LAT_N = (
    SELECT MAX(LAT_N)
    FROM station
    WHERE LAT_N < 137.2345
);
```
