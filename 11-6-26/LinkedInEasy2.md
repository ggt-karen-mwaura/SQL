# Duplicate Job Listings

**Difficulty:** Easy  
**Problem:** [DataLemur - Duplicate Job Listings](https://datalemur.com/questions/duplicate-job-listings)

## Intuition

Treat listings as duplicates when the same company has multiple rows with the same title and description. The CTE counts listings for each company/title/description combination; the outer query counts each company only once if any combination occurs more than once.

## Solution

```sql
WITH job_counts AS (
  SELECT company_id, COUNT(*) AS cnt
  FROM job_listings
  GROUP BY company_id, title, description
)
SELECT COUNT(DISTINCT company_id) AS duplicate_companies
FROM job_counts
WHERE cnt > 1;
```
