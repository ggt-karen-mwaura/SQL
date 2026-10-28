# Weather Observation Station 20

**Problem:** [Weather Observation Station 20](https://www.hackerrank.com/challenges/weather-observation-station-20/problem)

## Intuition

The median latitude is the value with the same number of observations below it as above it. For each station, the two subqueries count those lower and higher latitudes. The row where the counts are equal is the median, and rounding its latitude to four decimal places gives the requested result.

## Solution

```sql
SELECT ROUND(S.LAT_N, 4)
FROM STATION S
WHERE (SELECT COUNT(*) FROM STATION WHERE LAT_N < S.LAT_N) =
      (SELECT COUNT(*) FROM STATION WHERE LAT_N > S.LAT_N);
```
