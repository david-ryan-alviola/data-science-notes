# 7-JAN-2021

## Case Statements

* Temporary table review
    * `MODIFY` keyword used for changing column definition
        * `ALTER TABLE table MODIFY column TYPE(...);`
* Conditionals
    * `IF()`
        * returns value when condition is true
        * best when only evaluating true or false
        * `...IF(column = condition_1, value_1, value_2) AS new_column...`
    * used when more than 2 optional values or need more flexibility in other conditional tests
    * Limitations
        1. Can only check for equality
        2. Cannot test for null
        3. Case value can only come from one column.
    * `WHEN`
        * `...CASE column WHEN condition_a THEN value_1 WHEN condition_b THEN value_2 ELSE value_3 END AS new_column...`
            * output from case statement is put into new column 
