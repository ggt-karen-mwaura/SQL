# Weather Observation Station 11

- Link: https://www.hackerrank.com/challenges/weather-observation-station-11/problem
- Difficulty: Easy

## Intuition
We want to keep only cities that are not both starting and ending with a vowel. The pattern `^[AEIOU].*[AEIOU]$` matches cities whose first character is a vowel and whose last character is also a vowel. By adding `NOT`, we exclude those cases and keep the remaining cities. Using `DISTINCT` removes duplicate city names from the result.

## Solution
```sql
SELECT DISTINCT city
FROM station
WHERE city NOT REGEXP '^[AEIOU].*[AEIOU]$';
```