# New Companies

**Problem:** [New Companies](https://www.hackerrank.com/challenges/the-company/problem)

## Intuition

Each company can have multiple employees at every organizational level. Joining all levels directly can multiply rows, so count each level's codes distinctly. Use `LEFT JOIN` to retain companies even when a level has no matching records, group by company and founder, and sort by company code.

## Solution

```sql
SELECT
    c.company_code,
    c.founder,
    COUNT(DISTINCT l.lead_manager_code),
    COUNT(DISTINCT s.senior_manager_code),
    COUNT(DISTINCT m.manager_code),
    COUNT(DISTINCT e.employee_code)
FROM Company c
LEFT JOIN Lead_Manager l
    ON c.company_code = l.company_code
LEFT JOIN Senior_Manager s
    ON c.company_code = s.company_code
LEFT JOIN Manager m
    ON c.company_code = m.company_code
LEFT JOIN Employee e
    ON c.company_code = e.company_code
GROUP BY
    c.company_code,
    c.founder
ORDER BY c.company_code;
```
