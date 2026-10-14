# Revising the Select Query II

**Link:** [Hackerrank - Revising the Select Query II](https://www.hackerrank.com/challenges/revising-the-select-query-2/submissions/code/485201866)

## Intuition
We are asked to list the names of cities in the United States with a population greater than 120,000. Filtering by both the population threshold and the country code narrows the result to the exact set required.

## Solution
```sql
SELECT name
FROM city
WHERE population > 120000
AND countrycode = 'USA';
```
