https://blog.logrocket.com/create-backend-api-with-rust-postgres/



➜  ~ psql -d diesel_demo -U maarunipandithurai -W
Password:
psql (14.4)
Type "help" for help.

diesel_demo=# \l

diesel_demo-# \dt
                        List of relations
 Schema |            Name            | Type  |       Owner
--------+----------------------------+-------+--------------------
 public | __diesel_schema_migrations | table | maarunipandithurai
                                                  List of databases
         Name          |       Owner        | Encoding | Collate | Ctype |             Access privileges
-----------------------+--------------------+----------+---------+-------+-------------------------------------------
 book_app_development  | maarunipandithurai | UTF8     | C       | C     |
 book_app_test         | maarunipandithurai | UTF8     | C       | C     |
 chainlink             | maarunipandithurai | UTF8     | C       | C     |
 diesel_demo           | maarunipandithurai | UTF8     | C       | C     |
 diesel_demo2          | maarunipandithurai | UTF8     | C       | C     |
 graphql_todos_example | maarunipandithurai | UTF8     | C       | C     |
 postgres              | maarunipandithurai | UTF8     | C       | C     |
 streamsolana          | maarunipandithurai | UTF8     | C       | C     |
 suppliers             | maarunipandithurai | UTF8     | C       | C     |
 template0             | maarunipandithurai | UTF8     | C       | C     | =c/maarunipandithurai                    +
                       |                    |          |         |       | maarunipandithurai=CTc/maarunipandithurai
 template1             | maarunipandithurai | UTF8     | C       | C     | =c/maarunipandithurai                    +
                       |                    |          |         |       | maarunipandithurai=CTc/maarunipandithurai
 todosrust             | maarunipandithurai | UTF8     | C       | C     |
(12 rows)



                                                  List of databases
         Name          |       Owner        | Encoding | Collate | Ctype |      diesel_demo-# CREATE DATABASE emplydb
diesel_demo-# \l

diesel_demo=# CREATE DATABASE emplydb;
CREATE DATABASE
diesel_demo=# \l

diesel_demo=# \c emplydb
Password:
You are now connected to database "emplydb" as user "maarunipandithurai".
emplydb=# \dt
                        List of relations
 Schema |            Name            | Type  |       Owner
--------+----------------------------+-------+--------------------
 public | __diesel_schema_migrations | table | maarunipandithurai
 public | employees                  | table | maarunipandithurai
(2 rows)

emplydb=# select * from employees;
 id | first_name | last_name |       department       | salary | age
----+------------+-----------+------------------------+--------+-----
  2 | Mac        | Macintosh | Digital Transformation |   5000 |  20
(1 row)

emplydb=#