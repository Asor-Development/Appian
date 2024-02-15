## Integration
- allows Appian to call or use external systems
    - use integration objects with connected systems
    - then call your integrations in expression rules, interfaces, record types, or process models
- **Use to**
    - connect to a web service so you can use it as the source of a record type
    - query or modify data in third-party systems using the Call Integration smart service or using an expression
    - query and write data in a portal

## Connected System
- stores authentication and connection information so you can connect to external integrations and data sources
- **Use to** manage authentication details for a third-party system

## Web APIs
- allows other systems to contact Appian and expose Appian data and services to external systems
- **Use to**
    - expose an endpoint that external systems can call to complete an activity in Appian
        - sync data changed by a third-party system or changes made directly on the source
        - query and write data in a portal
        - query data from a record type or data store entity and display it in a third-party system
        - write data to a database from an external system
