# 5-JAN-2021

## Subqueries

* Queries within a query
    1. `SELECT * FROM table WHERE column IN (SELECT column FROM table WHERE column = value);`
    2. `SELECT * FROM (SELECT column_a, column_b FROM table);`