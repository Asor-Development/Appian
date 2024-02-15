# Appian Database
- you can configure and connect to your own supported relational databases
    -  maintaining your own database requires certain expertise 
- The Appian Cloud database is pre-configured so that you can focus on building low-code applications without any database set up

---

## Appian Cloud database
- is a MariaDB database server
- you can run a SELECT version() query in phpMyAdmin to determine the database version 
- Appian does not provide general assistance or training for using these databases because MariaDB is a widely adopted solution with abundant online documentation
- **uses phpMyAdmin as interface**
    - phpMyAdmin is a widely adopted solution with abundant online documentation, so Appian does not provide general assistance or training for using phpMyAdmin
    - the phpMyAdmin header has a different default color and label for development, testing, staging, and production environments
    - open a support case to change label or color

## Schemas
- **Schemas are visible to based on how your access is configured:**
    - **Cloud database access roles**
        - Database Adminstrators system group will be redirected to phpMyAdmin, where they can see all schemas in the database
        - Database Viewers and Editors system groups will see the specific schemas they have access to, along with the default Appian schema
    - **Schema-specific cloud database access**
        - Users that are granted separate read or write access to at least 1 schema using group types and user-created groups will see the specific schemas they have access to, along with the default Appian schema
- you can use schemas to control access to certain data
    - Appian cloud databases ship with a default "Appian" schema which has broad access
    - database administrators can create additional schemas and use system groups and object security to secure access to them
- **Best practices for creating additional schemas**
    - most of your data should be stored in the default "Appian" schema
    - it is recommended that you only create additional schemas when your applications need data segregation and isolation
    - it is recommended that you only create use one schema for that application in addition to the default "Appian" schema
    - if there are tables that are common to applications in your environment that use different data sources, create those tables in the "Appian" schema
        - For example, an Employee table that needs to be used in both Finance and HR applications should be created in the "Appian" schema
    - migrating data from existing schemas into new schemas is not recommended, only create schemas for new applications
- https://docs.appian.com/suite/help/23.4/appian-cloud-database-administration.html#granting-access-to-schemas

---
# Adding New Database/ Data Source
- Admin Console ---> Data Sources ---> New Data Source
    - Configure Data Source by providing type, connection string, username and password


----


## Summary
Appian Cloud database is a MariaDB database server that uses a phpAdmin interface.
- ship with a default `Appian` schema which has broad access, this is where most of your data should be stored
    - create additional schemas when your applications need data segregation and isolation
    - tables that are common to applications in your environment that use different data sources, create those tables in the "Appian" schema
- database administrators can create additional schemas and use system groups and object security to secure access to them