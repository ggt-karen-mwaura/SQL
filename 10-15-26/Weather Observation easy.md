# Weather Observation Station 12

**Problem:** [Weather Observation Station 12](https://www.hackerrank.com/challenges/weather-observation-station-12/problem)

## Intuition

Return each distinct city whose name does not both start and end with a vowel. The negated regular-expression match excludes names with vowels at both ends.

## Solution

```sql
SELECT DISTINCT city
FROM station
WHERE city NOT REGEXP '^[AEIOU].*[AEIOU]$';
```
