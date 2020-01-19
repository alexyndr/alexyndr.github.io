## PSQL

---

### - Setup

`sudo -u postgres psql` or `psql -U postgres`

postgres=#

`\connect`

=# You are now connected to database "postgres" as user "postgres"

---

### - Create Table

`CREATE TABLE citys (id INT NOT NULL, name VARCHAR(255));` *Column cannot consist nil* **NOT NULL**

`\d`

=# List of relations  
 Schema | Name  | Type  |  Owner 
---|---|---|--- 
public | citys | table | postgres 

(1 row)

---

### - Delete Table

`DROP TABLE citys;`

---

### - Insert 

`INSERT INTO citys(id, name)VALUES(1, 'String');`

=# INSERT 0 1

---

### - Select

`SELECT name FROM citys;`

| name |
|------| 
|String |
|String2|

(2 rows)  

`SELECT * FROM citys LIMIT 2;` *You can use* **LIMIT** *for set count of rows* 

| id |  name |
|---:|:------|
| 1 | String |
| 2 | String2|

(2 rows)

`SELECT * FROM citys WHERE name = String2;` *You can use other operators* **!= > >= < <=**

| id |  name |
|---:|:------|
| 2 | String2|

(1 row)

---

### - Update

`UPDATE citys SET name = 'new String';` *Change name for all records*

`UPDATE citys SET name = 'String' WHERE id = 2;` *Change name for one record with id = 2*

---

### - Delete

`DELETE FROM citys WHERE id = 1;`

---

### - Sorting

`SELECT * FROM citys ORDER BY id DESC;` *You can use other operators* **DESC ASC**

| id |    name  |
|----|:---------|
| 3 | String 3  |
| 2 | String 2  |
| 1 | String 1  |

(3 rows)

---

### - Add column

`ALTER TABLE citys ADD COLUMN death BOOLEAN NOT NULL DEFAULT TRUE;`

---

### - Delete column

`ALTER TABLE citys DROP COLUMN death;`

---

### - Rename column

`ALTER TABLE citys RENAME death TO life;`

---

### - Change type column

`ALTER TABLE citys ALTER COLUMN life SET DATA TYPE VARCHAR(255);`

---

### - Rename Table

`ALTER TABLE citys RENAME TO districts;`
