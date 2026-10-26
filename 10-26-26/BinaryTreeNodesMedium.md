# Binary Tree Nodes

**Problem:** [Binary Tree Nodes](https://www.hackerrank.com/challenges/binary-search-tree-1/problem)

## Intuition

The parent value identifies a root: its parent is `NULL`. A node is an inner node if its value appears as a parent value for another row. Any other node is a leaf. A `CASE` expression checks these conditions in that order, and sorting by `N` returns the results in ascending order.

## Solution

```sql
SELECT
    N,
    CASE
        WHEN P IS NULL THEN 'Root'
        WHEN N IN (SELECT P FROM BST) THEN 'Inner'
        ELSE 'Leaf'
    END
FROM BST
ORDER BY N;
```
