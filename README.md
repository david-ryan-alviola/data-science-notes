# 4-JAN-2021

## Relationships

* Indexes
    * used to improve performance when searching through a table
        * Without an index or indicies, the search would take place sequentially through the whole table.
    * `UNIQUE` constraint does not allow duplicate values to be present in that column
    * The primary key is the minimum index we will set.
    * Foreign keys (FK)
        * the primary key (PK) of another table
        * used to join two tables together
* `JOIN`
    * default join is an inner join
        * finds records from table A that correspond to a key on table B
            * don't return nulls by default
    * Relationships
        1. one to one
            * username and password
            * expressed with columns on the same table
        2. one to many
            * one employee could have many salaries
            * one employee could have many titles
            * the "many" table will have a FK that points to the "one" table
        3. many to many
            * one employee could belong to multiple departments (over time)
            * usually have an associative table like dept_emp to point to two other tables
            * A table with multiple FKs is usually indicative of a many:many relationship
        * Relationships help keep duplication of data to a minimum which increases efficiency
    * `SELECT columns FROM table_a AS a JOIN table_b AS b ON a.pk_id = b.fk_id;`
        * shortcut if PK and FK have the same name
            * `SELECT * FROM table_a JOIN table_b USING(column_name);`
            * also condenses the output to only have one column for PK and FK
    * `LEFT JOIN`
        * keeps any records from table A that have nulls to table B
        * the table after the `FROM` clause is the left table
    * `RIGHT JOIN`
        * keeps any records from table B that have a null on table A
        * the table after the `RIGHT JOIN` clause is the right table
    * Can accomplish right join with `LEFT JOIN` clause by swapping table orders and vice versa.
    * The number of joins is generally:  # of tables - 1
    
