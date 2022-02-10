# MySql-comments

show databases;

+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| performance_schema |
| sys                |
+--------------------+
4 rows in set (0.00 sec)

Create database blazers;<br>
Query OK, 1 row affected (0.01 sec)

 Show databases;

+--------------------+
| Database           |
+--------------------+
| blazers            |
| information_schema |
| mysql              |
| performance_schema |
| sys                |
+--------------------+
5 rows in set (0.00 sec)


Use blazers;
  Database changed

Create table students(id int primary key auto_increment,name varchar(25) not null,age int(2) not null,gender char(3)not null);<br>
   Query OK, 0 rows affected, 1 warning (0.04 sec)


Show tables;
+-------------------+
| Tables_in_blazers |
+-------------------+
| students          |
+-------------------+
1 row in set (0.00 sec)


Desc students;
+--------+-------------+------+-----+---------+----------------+
| Field  | Type        | Null | Key | Default | Extra          |
+--------+-------------+------+-----+---------+----------------+
| id     | int         | NO   | PRI | NULL    | auto_increment |
| name   | varchar(25) | NO   |     | NULL    |                |
| age    | int         | NO   |     | NULL    |                |
| gender | char(3)     | NO   |     | NULL    |                |
+--------+-------------+------+-----+---------+----------------+
4 rows in set (0.00 sec)


Insert into students (name,age,gender) values('Haiden',19,'M');<br>
    Query OK, 1 row affected (0.01 sec)


Insert into students (name,age,gender) values('Aswath',17,'M');<br>
    Query OK, 1 row affected (0.01 sec)


Select *from students;
+----+--------+-----+--------+
| id | name   | age | gender |
+----+--------+-----+--------+
|  1 | Haiden |  19 | M      |
|  2 | Aswath |  17 | M      |
+----+--------+-----+--------+
2 rows in set (0.00 sec)


Select * from students where id=1;
+----+--------+-----+--------+
| id | name   | age | gender |
+----+--------+-----+--------+
|  1 | Haiden |  19 | M      |
+----+--------+-----+--------+
1 row in set (0.00 sec)


Alter table students add degree varchar(20);<br>
    Query OK, 0 rows affected (0.03 sec)
    Records: 0  Duplicates: 0  Warnings: 0


Select *from students;
+----+--------+-----+--------+--------+
| id | name   | age | gender | degree |
+----+--------+-----+--------+--------+
|  1 | Haiden |  19 | M      | NULL   |
|  2 | Aswath |  17 | M      | NULL   |
+----+--------+-----+--------+--------+
2 rows in set (0.00 sec)


Update students set degree='+2' where id=1;<br>
    Query OK, 1 row affected (0.01 sec)
    Rows matched: 1  Changed: 1  Warnings: 0


Select *from students;
+----+--------+-----+--------+--------+
| id | name   | age | gender | degree |
+----+--------+-----+--------+--------+
|  1 | Haiden |  19 | M      | +2     |
|  2 | Aswath |  17 | M      | NULL   |
+----+--------+-----+--------+--------+
2 rows in set (0.00 sec)


Delete from students where id=1;<br>
    Query OK, 1 row affected (0.00 sec)


Select *from students;
+----+--------+-----+--------+--------+
| id | name   | age | gender | degree |
+----+--------+-----+--------+--------+
|  2 | Aswath |  17 | M      | NULL   |
+----+--------+-----+--------+--------+
1 row in set (0.00 sec)
















  
