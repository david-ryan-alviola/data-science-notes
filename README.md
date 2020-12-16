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
* Basic commands
    * `USE database_name` switches the database you are working in.
    * `SELECT DATABASE()` shows which database you are working in.
        * Notice that this is a function call
    * `SHOW CREATE DATABASE database_name` shows you the command used to create that database.