# Weather Observation Station 18

**Problem:** [Weather Observation Station 18](https://www.hackerrank.com/challenges/weather-observation-station-18/problem)

## Intuition

The Manhattan distance between the extreme station coordinates is the latitude range plus the longitude range. Subtract each minimum from its maximum, add the two differences, then round the result to four decimal places.

## Solution

```sql
SELECT ROUND(
    (MAX(LAT_N) - MIN(LAT_N)) +
    (MAX(LONG_W) - MIN(LONG_W)),
    4
)
FROM station;
```
