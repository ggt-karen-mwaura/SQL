# Ollivander's Inventory

**Difficulty:** Medium  
**Problem:** [HackerRank - Ollivander's Inventory](https://www.hackerrank.com/challenges/harry-potter-and-wands/problem)

## Intuition

Only non-evil wands should be considered. Wands with the same code share the same age, so for each `(code, power)` group we need the least expensive wand. A windowed `MIN` calculates that price without collapsing the wand rows; filtering to rows at that minimum keeps the required wand IDs. Finally, ordering by power and age in descending order matches the requested output.

## Solution

```sql
SELECT id, age, coins_needed, power
FROM (
    SELECT w.id, p.age, w.coins_needed, w.power,
           MIN(w.coins_needed) OVER (PARTITION BY w.code, w.power) AS min_coins
    FROM Wands w
    JOIN Wands_Property p ON w.code = p.code
    WHERE p.is_evil = 0
) t
WHERE coins_needed = min_coins
ORDER BY power DESC, age DESC;
```
