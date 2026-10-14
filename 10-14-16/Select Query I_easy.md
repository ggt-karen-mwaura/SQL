# Revising the Select Query I

**Link:** [Hackerrank - Revising the Select Query I](https://www.hackerrank.com/challenges/revising-the-select-query/problem)

## Intuition
This query selects all city records in the United States where the population exceeds 100,000. By combining a population condition with a country code filter, we isolate the cities that match the challenge requirements exactly.

## Solution
```sql
SELECT *
FROM city
WHERE population > 100000
AND countrycode = 'USA';
```