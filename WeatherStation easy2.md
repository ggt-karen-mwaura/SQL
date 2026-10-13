# Weather Observation Station 10

- Link: https://www.hackerrank.com/challenges/weather-observation-station-10/problem
- Difficulty: Easy

## Intuition
We only want cities whose names do not end with a vowel. The expression `[AEIOU]$` matches a city whose last character is a vowel. By applying `NOT`, we exclude those names and keep only cities ending with a consonant. The `DISTINCT` clause removes duplicate city names.

## Solution
```sql
SELECT DISTINCT city
FROM station
WHERE city NOT REGEXP '[AEIOU]$';
```
