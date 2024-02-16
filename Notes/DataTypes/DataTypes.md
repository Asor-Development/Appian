# Appian Data Types

- data must conform to certain data types
- data types can be
    - system types
    - Any Type
    - Map Type
    - custom data type 
    - Java object
    - imported from a WSDL by the Call Web Service smart service

## System Data Types
- is a required format for data stored in Appian
- includes primitive types and complex types
- each system data type can be used to store either a single value or a list of values

### Primitive System Data types
- there are 8 
    - text
    - time
    - number(decimal)
    - number(integer)
    - booleans
    - date
    - date time
    - encrypted text
---
### Complex System Data Types
- are made available in the system to support smart services and cannot be modified or deleted
- XML structure is not guaranteed to remain the same from release to release
- **ApplicationTestResult:** designed to hold test result information for all expression rules in an application
- **DataSubset:** designed to hold the data returned by a query configured with a paging parameter
- **EntityData:** lets you define a target data store entity and the values to store in the target entity as an input value for the Write to Multiple Data Store Entities Smart Service
- **EntityDataIdentifiers:** lets you define a target data store entity and the values to delete from the target entity as an input value for the Delete from Data Store Entities Smart Service
- **HealthCheckOutput:**
- **IntegrationError:**
- **LabelValue:**
- **LabelValueTable:**
- **ListViewItem:**
- **Facet:**
- **FacetOption:**
- **ObjectTestResult:**
- **PagingInfo:**
- **ProcessInfo:**
- [More](https://docs.appian.com/suite/help/23.4/Appian_Data_Types.html)
- **:**
- **:**
- **:**
- **:**
- **:**
- **:**
---

## Custom Data Types (CDTs)
- object that contains user defined fields, paired with their associated data types
- built from an XML Schema Definition (XSD)
- used to group related data ponits to be usde as a reference throughout app development
- does not store data it supports the organization of the data
- helps makes sure related data stays together
- to reference a CDT in and expression `type!nameOfObject`()

---

