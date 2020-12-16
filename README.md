# 16DEC2020

## SQL and MySQL

1. You were provided with a host address, username, and password.
    * Record it somewhere! Don't rely on Slack.
    * See sqlPasswords.txt
2. Structured Query Language (SQL)
    * MySQL, Oracle, MSSQL, PostGreSQL are different flavors
3. Databases provide a more efficient way to store info than your file system.
4. Data manipulation language (DML)
    * Create, retrieve, update, delete (CRUD) operations
5. SequelPro is the relational database management system (RDBMS) we will be using
    * command + R is the shortcut to run a single statement
6. Example statements
    * `SELECT * FROM mysql.user;` shows all columns from user table
    * `SELECT user, host FROM mysql.user` shows user and host columns from user table
    * `SELECT * FROM mysql.help_topic` shows all columns from help_topic table
    * `SELECT help_topic_id, help_category_id, url FROM mysql.help_topic` shows topic_id, category_id, and url from help_topic table