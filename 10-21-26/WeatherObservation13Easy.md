# Weather Observation Station 13

**Problem:** [Weather Observation Station 13](https://www.hackerrank.com/challenges/weather-observation-station-13/problem)

## Intuition

Filter stations to the specified latitude range, sum the remaining latitudes, and round the total to four decimal places.

## Solution

```sql
SELECT ROUND(SUM(LAT_N), 4)
FROM station
WHERE LAT_N > 38.7880
  AND LAT_N < 137.2345;
```
