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