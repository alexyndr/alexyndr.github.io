## PSQL

### - Setup

`sudo -u postgres psql` or `psql -U postgres`

postgres=#

`\connect`

=# You are now connected to database "postgres" as user "postgres".

### - Create

`create table citys (id INT, name VARCHAR(255));`

=# CREATE TABLE

`\d`

=# List of relations  
Schema | Name  | Type  |  Owner  
--------+-------+-------+----------  
 public | citys | table | postgres  
(1 row)

### - Delete

`drop table citys;`

=# DROP TABLE

### - Insert

`insert into citys(id, name) values(1, 'String');`

=# INSERT 0 1

### - Select

`select * from citys limit 2;` *You can use LIMIT for set count of rows* 

 id |  name   
----+---------  
  1 | String  
  2 | String2  
(2 rows)

`select * from citys where name = String2;` *You can use other operators* **!= > >= < <=**

 id |  name   
----+---------  
  2 | String2  
(1 row)

