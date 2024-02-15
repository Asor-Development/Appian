# Appian MariaDB
**Appian Cloud database is a MariaDB database server that uses a phpAdmin interface**

## Creating tables
- can create tables using SQL or can click `New` under `Appian ---> Tables ---> New` in the left palette
- Application prefix should be used when creating tables
### Right Panel
- Appian
    - **Functions:**
    - **Procedures:**
    - **Tables:** there are different types of tables
        - Data Tables: used to store the data, we can read, write etc...
        - Metric tables: 
        - has a `New` that can be clicked to create tables
### Tabs
**With no Tables Selected**

- **Structure:**
- **SQL:**
- **Search:**
- **Query:**
- **Export:**
- **Import:**
- **Operations:**
- **Routines:**
- **Events:**
- **Triggers:**
- **Designe:**

**With Table Selected**


- **Browser:** see the data in a table
- **Structure:** see the structure of a table
- **SQL:** allow us to write SQL queries
- **Search:** search the data using some of the data elements
- **Insert:** allow us to insert data manually
- **Export:** for deployment
- **Import:** for deployment
- **Operations:** do some operations such as change table name, copy, delete, change structure etc... 
- **Triggers:**



## Adding New Database/ Data Source
- Admin Console ---> Data Sources ---> New Data Source
    - Configure Data Source by providing type, connection string, username and password


### Using the data
- when a table is created from the database, we need to created a CDT or record type to be able to use the data in Appian