# Average Population of Each Continent

- **Difficulty:** Easy
- **Problem:** [HackerRank - Average Population of Each Continent](https://www.hackerrank.com/challenges/average-population-of-each-continent/problem)

## Intuition

Join cities to their countries so each city's population is associated with its continent. Group by continent, calculate the average city population in each group, and use `FLOOR` to round each result down to an integer.

## Solution

```sql
SELECT CO.Continent, FLOOR(AVG(CI.population))
FROM CITY AS CI
JOIN COUNTRY AS CO
    ON CI.CountryCode = CO.Code
GROUP BY CO.Continent;
```
