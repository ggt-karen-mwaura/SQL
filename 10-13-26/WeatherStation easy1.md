# Weather Observation Station 9

- Link: https://www.hackerrank.com/challenges/weather-observation-station-9/problem
- Difficulty: Easy

## Intuition
We need cities whose names do not start with a vowel. The pattern `^[AEIOU]` matches any city beginning with A, E, I, O, or U. By using `NOT REGEXP`, we filter out those city names and keep only names that begin with a consonant. `DISTINCT` ensures the final output contains each city only once.

## Solution
```sql
SELECT DISTINCT city
FROM station
WHERE city NOT REGEXP '^[AEIOU]';
```
