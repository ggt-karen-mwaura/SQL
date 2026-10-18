# Weather Observation Station 12

**Problem:** [Weather Observation Station 12](https://www.hackerrank.com/challenges/weather-observation-station-12/problem)

## Intuition

Return each city only once, and filter out any city whose name starts or ends with a vowel. The regular expression matches either a vowel at the beginning (`^[AEIOU]`) or a vowel at the end (`[AEIOU]$`); `NOT REGEXP` keeps names that match neither condition.

## Solution

```sql
SELECT DISTINCT CITY
FROM STATION
WHERE CITY NOT REGEXP '^[AEIOU]|[AEIOU]$';
```