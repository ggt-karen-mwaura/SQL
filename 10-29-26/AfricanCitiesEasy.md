# African Cities

- **Difficulty:** Easy
- **Problem:** [HackerRank - African Cities](https://www.hackerrank.com/challenges/african-cities/problem)

## Intuition

Join each city to its country using the country code, then filter the joined rows to countries on the African continent. Selecting the city name returns the requested list.

## Solution

```sql
SELECT ci.NAME
FROM CITY AS ci
JOIN COUNTRY AS co
ON ci.COUNTRYCODE = co.CODE
WHERE co.CONTINENT = 'Africa';
```