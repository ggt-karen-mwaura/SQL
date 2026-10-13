# Occupations

- Link: https://www.hackerrank.com/challenges/occupations
- Difficulty: Medium

## Intuition
We need to display names in four columns: Doctor, Professor, Singer, and Actor. Each occupation has multiple people, so the key idea is to assign a row number inside each occupation. Once each person's name is matched to its relative position in that occupation, we can place names from the same rank into the same output row across columns.

For example, the 1st doctor, 1st professor, 1st singer, and 1st actor should appear on the same row. The 2nd doctor, 2nd professor, and so on should appear on the next row. Using `ROW_NUMBER()` over each occupation lets us align the lists by index, and then `MAX(CASE ...)` picks the correct name for each column in each row.

## Solution
```sql
SELECT
    MAX(CASE WHEN Occupation = 'Doctor' THEN Name END) AS Doctor,
    MAX(CASE WHEN Occupation = 'Professor' THEN Name END) AS Professor,
    MAX(CASE WHEN Occupation = 'Singer' THEN Name END) AS Singer,
    MAX(CASE WHEN Occupation = 'Actor' THEN Name END) AS Actor
FROM (
    SELECT
        Name,
        Occupation,
        ROW_NUMBER() OVER (PARTITION BY Occupation ORDER BY Name) AS rn
    FROM OCCUPATIONS
) AS ranked
GROUP BY rn
ORDER BY rn;
```