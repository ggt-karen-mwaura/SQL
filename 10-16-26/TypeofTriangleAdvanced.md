# Type of Triangle

**Problem:** [Type of Triangle](https://www.hackerrank.com/challenges/what-type-of-triangle/problem)

## Intuition

Check the triangle inequality first: the sum of any two sides must be greater than the third side. If any check fails, the sides cannot form a triangle. For valid triangles, equal side lengths determine whether the triangle is equilateral or isosceles; if no sides are equal, it is scalene.

## Solution

```sql
SELECT
    CASE
        WHEN A + B <= C
          OR A + C <= B
          OR B + C <= A
            THEN 'Not A Triangle'
        WHEN A = B AND B = C
            THEN 'Equilateral'
        WHEN A = B OR B = C OR A = C
            THEN 'Isosceles'
        ELSE 'Scalene'
    END
FROM TRIANGLES;
```
