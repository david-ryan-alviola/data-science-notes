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