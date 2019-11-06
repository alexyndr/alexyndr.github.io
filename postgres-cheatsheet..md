## PSQL

### - Setup

`sudo -u postgres psql` or `psql -U postgres`

postgres=#

`\connect`

=# You are now connected to database "postgres" as user "postgres".

### - Create

`CREATE TABLE citys (id INT NOT NULL, name VARCHAR(255));` *Column cannot consist nil* **NOT NULL**

=# CREATE TABLE

`\d`

=# List of relations  
Schema | Name  | Type  |  Owner  
--------+-------+-------+----------  
 public | citys | table | postgres  
(1 row)

### - Delete

`DROP TABLE citys;`

=# DROP TABLE

### - Insert

`INSERT INTO citys(id, name)VALUES(1, 'String');`

=# INSERT 0 1

### - Select

`SELECT * FROM citys LIMIT 2;` *You can use* **LIMIT** *for set count of rows* 

 id |  name   
----+---------  
  1 | String  
  2 | String2  
(2 rows)

`SELECT * FROM citys WHERE name = String2;` *You can use other operators* **!= > >= < <=**

 id |  name   
----+---------  
  2 | String2  
(1 row)

### - Update

`UPDATE citys SET name = 'new String';` *Change name for all records*

=# UPDATE 3

`UPDATE citys SET name = 'String' WHERE id = 2;` *Change name for one record with id = 2*

=# UPDATE 1
