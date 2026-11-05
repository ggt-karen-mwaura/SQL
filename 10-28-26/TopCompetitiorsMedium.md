# Top Competitors

- **Difficulty:** Medium
- **Problem:** [HackerRank - Full Score](https://www.hackerrank.com/challenges/full-score/problem)

## Intuition

Join submissions to each challenge's difficulty and maximum score, then keep only submissions that earned the full score. Group the qualifying submissions by hacker and count distinct challenges so repeated submissions do not inflate the total. Keep hackers who achieved full scores on more than one challenge and sort by that count descending, breaking ties by hacker ID ascending.

## Solution

```sql
SELECT h.hacker_id, h.name
FROM Submissions s
JOIN Challenges c ON s.challenge_id = c.challenge_id
JOIN Difficulty d ON c.difficulty_level = d.difficulty_level
JOIN Hackers h    ON s.hacker_id = h.hacker_id
WHERE s.score = d.score
GROUP BY h.hacker_id, h.name
HAVING COUNT(DISTINCT s.challenge_id) > 1
ORDER BY COUNT(DISTINCT s.challenge_id) DESC, h.hacker_id ASC;
```
