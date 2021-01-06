# 6-JAN-2021

## Temporary Tables

* `TEMPORARY` keyword
    * similar syntax to creating a permanent table, but `TEMPORARY` is added
    * `CREATE TEMPORARY TABLE table_name(...)`
    * can be used for data manipulations without modifying the source data
        * can create and populate temporary tables using data from tables in different databases
            1. `SELECT * FROM database.table`
                * must specify database since you will be using a different DB
            2. `CREATE TEMPORARY TABLE table_name AS (select_statement_above)`
