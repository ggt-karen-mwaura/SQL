# Population Census

**Problem:** [Population Census](https://www.hackerrank.com/challenges/asian-population/problem)

## Intuition

Each city is linked to its country through the city's country code and the country's code. Joining those tables makes the continent available for filtering. Restrict the rows to Asian countries, then sum the population of their cities.

## Solution

```sql
SELECT SUM(C.population)
FROM city AS C
INNER JOIN country AS CO
    ON C.countrycode = CO.code
WHERE CO.continent = 'Asia';
```