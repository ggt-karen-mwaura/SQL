# Weather Observation Station 5

**Problem:** [Weather Observation Station 5](https://www.hackerrank.com/challenges/weather-observation-station-5/problem)

## Intuition

Find the shortest and longest city names separately. In each query, sort by name length and use the city name alphabetically to break ties, then combine the two rows.

## Solution

```sql
(SELECT city, LENGTH(city)
FROM station
ORDER BY LENGTH(city) ASC, city ASC
LIMIT 1)

UNION ALL

(SELECT city, LENGTH(city)
FROM station
ORDER BY LENGTH(city) DESC, city ASC
LIMIT 1);
```
