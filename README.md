# trivia_quiz
# TRIVIA APPLICATION 

It is an application which is an user-interactive quiz application.

Installations:
1. Ruby
2. Rails
3. MySQL

Database: creation of tables 

1. I created an admin - "quizadmin" and granted all the privileges for 
"trivia_quiz_development" database.

C:\xampp\mysql\bin>mysql -u quizadmin -p
Enter password: ********
Welcome to the MariaDB monitor.  Commands end with ; or \g.
Your MySQL connection id is 86
Server version: 5.7.20-log MySQL Community Server (GPL)

Copyright (c) 2000, 2017, Oracle, MariaDB Corporation Ab and others.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

MySQL [(none)]> show databases;
+-------------------------+
| Database                |
+-------------------------+
| information_schema      |
| trivia_quiz_development |
+-------------------------+
2 rows in set (0.35 sec)

MySQL [(none)]> use trivia_quiz_development;
Database changed

MySQL [trivia_quiz_development]> show tables;
+-----------------------------------+
| Tables_in_trivia_quiz_development |
+-----------------------------------+
| answers                           |
| ar_internal_metadata              |
| quizzes                           |
| schema_migrations                 |
| users                             |
+-----------------------------------+
5 rows in set (0.06 sec)

MySQL [trivia_quiz_development]>

MySQL [trivia_quiz_development]> describe users;
+------------+--------------+------+-----+---------+----------------+
| Field      | Type         | Null | Key | Default | Extra          |
+------------+--------------+------+-----+---------+----------------+
| id         | int(11)      | NO   | PRI | NULL    | auto_increment |
| password   | varchar(255) | YES  |     | NULL    |                |
| email      | varchar(255) | YES  |     | NULL    |                |
| created_at | datetime     | NO   |     | NULL    |                |
| updated_at | datetime     | NO   |     | NULL    |                |
+------------+--------------+------+-----+---------+----------------+
5 rows in set (0.13 sec)


MySQL [trivia_quiz_development]> describe quizzes;
+-------------+--------------+------+-----+---------+----------------+
| Field       | Type         | Null | Key | Default | Extra          |
+-------------+--------------+------+-----+---------+----------------+
| id          | int(11)      | NO   | PRI | NULL    | auto_increment |
| title       | varchar(255) | YES  |     | NULL    |                |
| description | varchar(255) | YES  |     | NULL    |                |
| user_id     | int(11)      | YES  |     | NULL    |                |
| created_at  | datetime     | NO   |     | NULL    |                |
| updated_at  | datetime     | NO   |     | NULL    |                |
+-------------+--------------+------+-----+---------+----------------+
6 rows in set (0.00 sec)


MySQL [trivia_quiz_development]> describe answers;
+------------+--------------+------+-----+---------+----------------+
| Field      | Type         | Null | Key | Default | Extra          |
+------------+--------------+------+-----+---------+----------------+
| id         | int(11)      | NO   | PRI | NULL    | auto_increment |
| answer     | varchar(255) | YES  |     | NULL    |                |
| userid     | varchar(255) | YES  |     | NULL    |                |
| quiz_id    | int(11)      | YES  | MUL | NULL    |                |
| created_at | datetime     | NO   |     | NULL    |                |
| updated_at | datetime     | NO   |     | NULL    |                |
+------------+--------------+------+-----+---------+----------------+
6 rows in set (0.00 sec)


