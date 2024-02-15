# Maria DB

## Creating A Database

`CREATE DATABASE musicstore`
    - create a sub-directory called musicstore
    - sets up a place to add tables
`USE musicstore;`
    - sets this new database as the default database
    - will remain your default until you change it to a different one or until you log out of MariaDB


- create a simple table that will hold basic data on books
        -         CREATE TABLE records (fieldname type, fieldname type, fieldname type)

        CREATE TABLE records (id CHAR(20) PRIMARY KEY, 
        title VARCHAR(50),
        author_id INT,
        publisher_id INT,
        year_pub CHAR(4),
        description TEXT );

- CHAR(20),
- VARCHAR(50)
- INT