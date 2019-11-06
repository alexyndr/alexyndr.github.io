## PSQL

### Setup

`sudo -u postgres psql` or `psql -U postgres`

postgres=#

`\connect`

=# You are now connected to database "postgres" as user "postgres".

### Create

`create table citys (id INT, name VARCHAR(255));`

=# CREATE TABLE

`\d`

 ```Schema | Name  | Type  |  Owner   
--------+-------+-------+----------
 public | citys | table | postgres
(1 row)```
