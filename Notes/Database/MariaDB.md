# Maria DB


- PRIMARY KEY: 

### DATA TYPES
- CHAR(20): a fixed-width character type of 20 character
- VARCHAR(50): a variable width character column of fifty characters at most
- INT: integer
- TEXT: a variable width column and it can hold up to 65,535 bytes of data for each row
## Creating A Database

`CREATE DATABASE musicstore`
    - create a sub-directory called musicstore
    - sets up a place to add tables
`USE musicstore;`
    - sets this new database as the default database
    - will remain your default until you change it to a different one or until you log out of MariaDB


- create a simple table that will hold basic data on books
        - CREATE TABLE records (fieldname type, fieldname type, fieldname type)
         - creates the table records with three fields/columns


### ALTER TABLE 
- change the settings of a table


---


### DROP TABLE
- delete a table completely (including its data)