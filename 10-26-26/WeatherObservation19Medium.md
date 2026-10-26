# Weather Observation Station 19

**Problem:** [Weather Observation Station 19](https://www.hackerrank.com/challenges/weather-observation-station-19/problem)

## Intuition

The two points are formed by pairing the minimum latitude with the minimum longitude, and the maximum latitude with the maximum longitude. The requested distance is the Euclidean distance between those points: square each coordinate difference, add the squares, and take the square root. Round the result to four decimal places.

## Solution

```sql
SELECT ROUND(
    SQRT(
        POWER(MAX(LAT_N) - MIN(LAT_N), 2) +
        POWER(MAX(LONG_W) - MIN(LONG_W), 2)
    ),
    4
)
FROM STATION;
```
