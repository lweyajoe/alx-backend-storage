# 0x00-MySQL_Advanced

# Concepts
For this project, we expect you to look at this concept:

Advanced SQL

## Resources

### Read or watch:

1. [MySQL cheatsheet](https://devhints.io/mysql)
2. [MySQL Performance: How To Leverage MySQL Database Indexing](https://www.liquidweb.com/kb/mysql-optimization-how-to-leverage-mysql-database-indexing/)
3. [Stored Procedure](https://www.w3resource.com/mysql/mysql-procedure.php)
4. [Triggers](https://www.w3resource.com/mysql/mysql-triggers.php)
5. [Views](https://www.w3resource.com/mysql/mysql-views.php)
6. [Functions and Operators](https://dev.mysql.com/doc/refman/5.7/en/functions.html)
7. [Trigger Syntax and Examples](https://dev.mysql.com/doc/refman/5.7/en/trigger-syntax.html)
8. [CREATE TABLE Statement](https://dev.mysql.com/doc/refman/5.7/en/create-table.html)
9. [CREATE PROCEDURE and CREATE FUNCTION Statements](https://dev.mysql.com/doc/refman/5.7/en/create-procedure.html)
10. [CREATE INDEX Statement](https://dev.mysql.com/doc/refman/5.7/en/create-index.html)
11. [CREATE VIEW Statement](https://dev.mysql.com/doc/refman/5.7/en/create-view.html)

## Learning Objectives
At the end of this project, you are expected to be able to explain to anyone, without the help of Google:

### General
1. How to create tables with constraints
2. How to optimize queries by adding indexes
3. What is and how to implement stored procedures and functions in MySQL
4. What is and how to implement views in MySQL
5. What is and how to implement triggers in MySQL

## Requirements

### General
1. All your files will be executed on Ubuntu 18.04 LTS using ```MySQL 5.7``` (version 5.7.30)
2. All your files should end with a new line
3. All your SQL queries should have a comment just before (i.e. syntax above)
4. All your files should start by a comment describing the task
5. All SQL keywords should be in uppercase (```SELECT```, ```WHERE``` …)
6. A ```README.md``` file, at the root of the folder of the project, is mandatory
7. The length of your files will be tested using ```wc```

## More Info

### Comments for your SQL file:

```
$ cat my_script.sql
-- 3 first students in the Batch ID=3
-- because Batch 3 is the best!
SELECT id, name FROM students WHERE batch_id = 3 ORDER BY created_at DESC LIMIT 3;
$
```

### Use “container-on-demand” to run MySQL
* Ask for container ```Ubuntu 18.04 - Python 3.7```
* Connect via SSH
* Or via the WebTerminal
* In the container, you should start MySQL before playing with it:

```
$ service mysql start
 * MySQL Community Server 5.7.30 is started
$
$ cat 0-list_databases.sql | mysql -uroot -p my_database
Enter password: 
Database
information_schema
mysql
performance_schema
sys
$
```

In the container, credentials are ```root/root```

### How to import a SQL dump
```
$ echo "CREATE DATABASE hbtn_0d_tvshows;" | mysql -uroot -p
Enter password: 
$ curl "https://s3.amazonaws.com/intranet-projects-files/holbertonschool-higher-level_programming+/274/hbtn_0d_tvshows.sql" -s | mysql -uroot -p hbtn_0d_tvshows
Enter password: 
$ echo "SELECT * FROM tv_genres" | mysql -uroot -p hbtn_0d_tvshows
Enter password: 
id  name
1   Drama
2   Mystery
3   Adventure
4   Fantasy
5   Comedy
6   Crime
7   Suspense
8   Thriller
$
```
