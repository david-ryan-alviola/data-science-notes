# 18-DEC-2020

## SQL clauses (contd), functions, and `GROUP BY`

* `ORDER BY`
    * `SELECT column FROM table ORDER BY column_name [ASC|DESC];`
    * ordered by the primary key by default and ascending
    * can chain multiple orders
        * `...ORDER BY column1 ASC, column2 DESC;`
* `LIMIT`
    * `SELECT * FROM table LIMIT max`
        * returns no more than the max number of results specified
    * `OFFSET`
        * used in conjunction with `LIMIT`
        * `SELECT * FROM table LIMIT max OFFSET position;`
            * the specified position shifts where the returned results start
            * commonly used in pagination for web applications
        * `SELECT emp_no FROM employees LIMIT 10 OFFSET 10;`
            * shows the second batch of 10 employees assuming we have more than 10 employees
        * if you want a certain page of results it follows this formula:  offset = (limit * page) - limit
* Functions
    1. `CONCAT(column1, 'string', column2)`
        * concatenates the arguments
    2. `LIKE` and `NOT LIKE` are also functions.
    3. `SUBSTR(string, start_index, length)`
        * SQL indexes at position 1
    4. Case conversion
        1. `UPPER`
        2. `LOWER`  
    5. `REPLACE(subject, search, replacement)`
    6. Time
        1. `NOW()` - YYYY-MM-DD HH:MM:SS
        2. `CURDATE()` - YYYY-MM-DD
        3. `CURTIME()` - HH:MM:SS
        4. `UNIX_TIMESTAMP()` and `UNIX_TIMESTAMP(date)` - returns the number of seconds since 01-JAN-1970
    7. Numerical
        1. `AVG(column)` - average of values in column
        2. `MIN(column)` - minimum value in column
        3. `MAX(column)` - maximum value in column
    8. Casting
        * convert one data type into another
        * `SELECT CAST(123 AS CHAR), CAST('123' AS UNSIGNED);`
* `GROUP BY`
    * similar to `DISTINCT`, but also orders the results in ascending order by default
    * `SELECT salary FROM salaries GROUP BY salary DESC;`
    * Aggregate functions with `GROUP BY`
        * `COUNT()`, `MIN()`, `MAX()`, `AVG()`
        * ` SELECT CONCAT(first_name, ' ', last_name) AS full_name, COUNT(*) FROM employees GROUP BY full_name DESC ORDER BY count(*) DESC;`
            * the second column shows the number of counts for a given full_name
