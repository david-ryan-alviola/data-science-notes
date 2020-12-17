# 17DEC2020

## SQL Basic Statements

* CRUD operations
    1. Create - `INSERT`
    2. Read - `SELECT`
    3. Update - `UPDATE`
    4. Delete - `DELETE`
* Follow the standard of using the single quote to denote string values.
* Reading data
    * `SELECT column_name(s) FROM table_name;`
    * Using `*` in place of a specific column name retrieves all columns from a table.
    * Separate multiple column names with commas.
* Filtering results
    * `WHERE` clause
    * `SELECT * FROM table_name WHERE column_name = 'value';`
        * can use other operators besides `=`:  `>`,`<`,`!=`,`<>`,`<=`,`>=`,`!<`,`!>`, `BETWEEN min AND max`
* Aliases
    * `AS` keyword
        * `SELECT column_name AS alias FROM table`
        * `SELECT alias.column_name FROM table AS alias`
* Clauses
    * Wildcards (%)
        * `LIKE '%string_value%'`
        * `LIKE '%-12-17'`
        * Placement of the wildcard is used to specify if you want values starting, ending, or containing a specified value.
    * `AND`, `OR`, `NOT` operators
        * can chain together filter criteria
            1. `SELECT * FROM employees WHERE hire_date LIKE '%-12-17' AND birth_date LIKE '%-12-17';`
            2. `SELECT * FROM employees WHERE (hire_date LIKE '%-12-17' OR birth_date LIKE '%-12-17') AND NOT (hire_date LIKE '%-12-17' AND birth_date LIKE '%-12-17');`
    * `IN` operator
        * `SELECT * FROM table WHERE column IN (value1, value_2, value_3);`
            * Only returns results within the specified set
    * `IS NULL`, `IS NOT NULL`
        * `SELECT * FROM table WHERE column IS NOT NULL;`
        * specifies whether or not you want results that have null for that column