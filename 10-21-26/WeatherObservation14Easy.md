# Weather Observation Station 14

**Problem:** [Weather Observation Station 14](https://www.hackerrank.com/challenges/weather-observation-station-14/problem)

## Intuition

Exclude stations at or above the upper latitude bound, find the greatest remaining latitude with `MAX`, and round it to four decimal places.

## Solution

```sql
SELECT ROUND(MAX(LAT_N), 4)
FROM station
WHERE LAT_N < 137.2345;
```
