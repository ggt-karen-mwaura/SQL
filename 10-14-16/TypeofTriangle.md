# Type of Triangle

**Link:** [Hackerrank - Type of Triangle](https://www.hackerrank.com/challenges/what-type-of-triangle/copy-from/485207994)

## Intuition
This challenge checks the relationship between the three triangle sides. First, we determine whether the triangle is invalid by testing whether any side is too long to form a triangle. If it is valid, we then classify it as equilateral, isosceles, or scalene using the side comparisons.

## Solution
```sql
SELECT * ,
 CASE WHEN A= B AND B = C THEN 'Equilateral'
 
      WHEN A= B AND A <> C 
       OR A = C AND B <> A 
       OR B = C AND A <> B THEN 'Isosceles'
      
      WHEN A + B <= C
       OR B + C <= A
       OR A + C <= B THEN 'Not A Triangle'
       
       WHEN A <> B AND B <> C AND A <> C THEN 'Scalene'
    END AS TriangleType
    
FROM triangles;
```
