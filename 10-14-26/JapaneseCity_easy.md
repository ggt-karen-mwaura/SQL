# Japanese Cities' Attributes

**Link:** [Hackerrank - Japanese Cities' Attributes](https://www.hackerrank.com/challenges/japanese-cities-attributes/submissions/code/485200593)

## Intuition
The task is to retrieve all records for cities located in Japan. Since the country code for Japan is `JPN`, we can filter the `city` table to only include rows where `countrycode` matches that value.

## Solution
```sql
SELECT *
FROM city
WHERE countrycode ='JPN';
```
