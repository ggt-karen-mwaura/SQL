# Weather Observation Station 2

**Problem:** [Weather Observation Station 2](https://www.hackerrank.com/challenges/weather-observation-station-2/problem)

## Intuition

Add all station latitudes and longitudes separately, then round each total to two decimal places as required.

## Solution

```sql
SELECT
    ROUND(SUM(LAT_N), 2),
    ROUND(SUM(LONG_W), 2)
FROM station;
```
