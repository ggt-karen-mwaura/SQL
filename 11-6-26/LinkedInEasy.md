# Data Science Skills

**Difficulty:** Easy  
**Problem:** [DataLemur - Data Science Skills](https://datalemur.com/questions/matching-skills)

## Intuition

Filter to the three required skills, then group the remaining rows by candidate. A candidate qualifies if they have all three matching skills, so keep groups with a count of three. Sorting by candidate ID makes the output deterministic.

## Solution

```sql
SELECT candidate_id
FROM candidates
WHERE skill IN ('Python', 'Tableau', 'PostgreSQL')
GROUP BY candidate_id
HAVING COUNT(skill) = 3
ORDER BY candidate_id;
```