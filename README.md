# 16DEC2020

## SQL and MySQL

* You were provided with a host address, username, and password.
    * Record it somewhere! Don't rely on Slack.
    * See sqlPasswords.txt
* Structured Query Language (SQL)
    * MySQL, Oracle, MSSQL, PostGreSQL are different flavors.
* Databases provide a more efficient way to store info than your file system.
* Data manipulation language (DML)
    * Create, retrieve, update, delete (CRUD) operations
* SequelPro is the relational database management system (RDBMS) we will be using.
    * command + R is the shortcut to run a single statement.
* Example statements
    * `SELECT * FROM mysql.user;` shows all columns from user table.
    * `SELECT user, host FROM mysql.user` shows user and host columns from user table.
    * `SELECT * FROM mysql.help_topic` shows all columns from help_topic table.
    * `SELECT help_topic_id, help_category_id, url FROM mysql.help_topic` shows topic_id, category_id, and url from help_topic table.
* SQL is NOT case sensitive.
    * `select * from sql.table` == `SELECT * FROM SQL.TABLE`
    * I recommend using CAPS for key words and lowercase for names or vice versa to help differentiate
        * `SELECT column FROM sql.table` or `select COLUMN from SQL.TABLE` 
* Basic database level commands
    * `SHOW DATABASES` shows all databases available
    * `USE database_name` switches the database you are working in.
    * `SELECT DATABASE()` shows which database you are working in.
        * Notice that this is a function call
    * `SHOW CREATE DATABASE database_name` shows you the command used to create that database.
* Tables
    * Like a spreadsheet, but more strict
        * statically typed
    * Data types
        * Numeric types
            1. `INT` - whole numbers
            2. `FLOAT` - with decimals
            3. `DECIMAL` - specify length and precision
            4. `TINYINT` - used in place of boolean for MySQL (`0 = false`; `1 = true`)
        * String types
            1. `CHAR(length)` - short strings
            2. `VARCHAR(length)` - text up to 65535 characters
            3. `TEXT` - used to hold large blocks of text at a performance cost
            * Single quotes(`'`) used to indicate string values
        * Date types
            1. `DATE` - default `YYYY-MM-DD`
            2. `TIME` - 24 hour time down to seconds
            3. `DATETIME` - combined date and time:  `YYYY-MM-DD HH:MM:SS`
                * No timezone information
        * `NULL`
            * absence of a value
            * need to specify if columns accept null values or not
    * Creating tables
        * `CREATE TABLE table_name (column1_name data_type, column2_name data_type);`
        * `NOT NULL` prevents a column from accepting null values
            * declared after the data type
        * Primary keys
            1. Must be unique
            2. Cannot be null
            3. Only one primary key per table
            * Set primary key with `PRIMARY KEY (column_name)` after the last column declaration
    * Showing tables
        * `SHOW TABLES` shows all tables within a database
        * `DESCRIBE table_name` shows the table definitions
        * `SHOW CREATE TABLE table_name` shows the command use to create the table