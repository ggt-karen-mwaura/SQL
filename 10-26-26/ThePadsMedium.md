# The PADS

**Problem:** [The PADS](https://www.hackerrank.com/challenges/the-pads/problem)

## Intuition

The output has two parts. First, format each person's name with the first letter of their occupation in parentheses, then sort those rows by name. Second, count how many people have each occupation, lowercase the occupation name in the sentence, and sort the counts from smallest to largest. Sorting by occupation as a tie-breaker makes equal counts appear alphabetically.

## Solution

```sql
SELECT CONCAT(Name, '(', LEFT(Occupation, 1), ')')
FROM OCCUPATIONS
ORDER BY Name;

SELECT CONCAT(
    'There are a total of ',
    COUNT(*),
    ' ',
    LOWER(Occupation),
    's.'
)
FROM OCCUPATIONS
GROUP BY Occupation
ORDER BY COUNT(*), Occupation;
```
