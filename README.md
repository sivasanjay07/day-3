C:\Users\HP>cd..

C:\Users>cd..

C:\>cd xampp

C:\xampp>cd mysql

C:\xampp\mysql>cd bin

C:\xampp\mysql\bin>mysql.exe -u root
Welcome to the MariaDB monitor.  Commands end with ; or \g.
Your MariaDB connection id is 12
Server version: 10.4.25-MariaDB mariadb.org binary distribution

Copyright (c) 2000, 2018, Oracle, MariaDB Corporation Ab and others.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

MariaDB [(none)]> show  databases;
+--------------------+
| Database           |
+--------------------+
| bottle             |
| chandu             |
| customer           |
| information_schema |
| juli               |
| lucky              |
| mysql              |
| performance_schema |
| phpmyadmin         |
| sanjay             |
| sanju              |
| shiva              |
| siva               |
| student            |
| test               |
+--------------------+
15 rows in set (0.001 sec)

MariaDB [(none)]> use customer;
Database changed
MariaDB [customer]> create table customer(
    -> id int primary key,
    -> name varchar(20),
    -> age int
    -> );
Query OK, 0 rows affected (0.038 sec)

MariaDB [customer]> select * from customerable where age>30;
ERROR 1146 (42S02): Table 'customer.customerable' doesn't exist
MariaDB [customer]> select * from customer where age>30;
Empty set (0.001 sec)

MariaDB [customer]> select * from customer where age between 20 and 60;
Empty set (0.000 sec)

MariaDB [customer]> select * from customer where name like '%siva%';
Empty set (0.000 sec)

MariaDB [customer]> select * from customer where age in (25,30,35);
Empty set (0.000 sec)

MariaDB [customer]> desc customer;
+-------+-------------+------+-----+---------+-------+
| Field | Type        | Null | Key | Default | Extra |
+-------+-------------+------+-----+---------+-------+
| id    | int(11)     | NO   | PRI | NULL    |       |
| name  | varchar(20) | YES  |     | NULL    |       |
| age   | int(11)     | YES  |     | NULL    |       |
+-------+-------------+------+-----+---------+-------+
3 rows in set (0.026 sec)

MariaDB [customer]>







