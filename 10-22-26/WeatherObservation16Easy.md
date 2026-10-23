# Weather Observation Station 16

**Problem:** [Weather Observation Station 16](https://www.hackerrank.com/challenges/weather-observation-station-16/problem)

## Intuition

Keep only stations whose latitude is greater than the given lower bound, find the smallest qualifying latitude with `MIN`, and round it to four decimal places.

## Solution

```sql
SELECT ROUND(MIN(LAT_N), 4)
FROM station
WHERE LAT_N > 38.7780;
```
