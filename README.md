# SQL Challenge Solutions

This repository contains SQL practice solutions for HackerRank challenges, focused on filtering, string matching, ranking, and table transformations.

## Overview

The files in this project document both the intuition and the final SQL query for each problem. Each markdown file explains:

- the problem link
- the difficulty level
- the reasoning behind the solution
- the final SQL implementation

## Included Challenges

- Weather Observation Station 9
- Weather Observation Station 10
- Weather Observation Station 11
- Occupations

## Project Structure

```text
SQL/
├── README.md
├── WeatherStation easy1.md
├── WeatherStation easy2.md
├── WeatherStation easy3.md
├── Occupations medium1.md
└── 10/13/26/
    └── WeatherStation easy1.md
```

## Topics Covered

- `REGEXP` filtering for vowel rules
- `DISTINCT` usage to remove duplicate results
- conditional aggregation with `CASE` and `MAX()`
- window functions such as `ROW_NUMBER()`
- pivoting data by occupation

## Example

```sql
SELECT DISTINCT city
FROM station
WHERE city NOT REGEXP '^[AEIOU]';
```

This example shows the basic pattern used in several weather station problems: filter out names that begin with vowels and keep only valid results.

## Notes

These files are meant to help practice SQL logic and understand how to translate a problem into a working query. They can be used as a reference for revision, learning, or portfolio documentation.

## License

This project is intended for learning and personal practice purposes.
