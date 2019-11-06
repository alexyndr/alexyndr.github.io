## PSQL

* Setup

`sudo -u postgres psql` or `psql -U postgres`

postgres=#

`\connect`

=# You are now connected to database "postgres" as user "postgres".

### Create

`create table citys (id INT, name VARCHAR(255));`

=# CREATE TABLE

`\d`

=# List of relations  
Schema | Name  | Type  |  Owner  
--------+-------+-------+----------  
 public | citys | table | postgres  
(1 row)

### Delete

`drop table citys;`

=# DROP TABLE

### Insert

`insert into citys(id, name) values(1, 'String');`

=# INSERT 0 1

`select * from citys;`

 id |  name   
----+---------  
  1 | String  
  2 | String2  
  3 | String3  
(3 rows)
