# Record Type Object
**A record type is an Appian design object that enables you to configure Appian Records**
**When desinging an applications you should start with record types and they way you design them matters because user need to able to look at a record, find what they need and take action on it quickly**
- When creating a new record type you do not have to save it to a folder
- the plural name is what business users will see in their Site, so pick the name that will make sense to your business users
- field references are specific to each record type and environment
- there are scenarios when you need to use other objects in addition to or instead of a record type
    - when extracting data from a document, you’ll need a custom data type (CDT) to map data extracted from a document
    - if your data lives in a third-party system, you’ll need an integration to access that system before you can work with that data in Appian
**Use Record Types When**
- you want to view, display, and report on data from a database, process model, Salesforce, or other web service
- you want to add, update, or delete data from a database table
- connecting Appian data for portals
- **To accelerate application development:**
    - Relate data, regardless of where the data lives
    - Transform existing data into the insights you need
    - Generate record views and record actions
    - Apply record-level security to secure enterprise data
---

## Primary elements
- make up the record type object and contribute to how users will eventually see and interact with the data: 
1. **Record data**
    - define the source type(database, process, salesforce, web service)
    - data sync will query an internal version of you data(cache), data is closer to the user and increases the speed and performace of the record type 
    - if there is an issue syncing your data, ensure that the Skip Failed Syncs is turned on(Access the Data Sync tab), to use data from the last successful sync and to notify administrators, and see relevant details are shown under Sync History
    - you can select and configure the fields you want to see in the record type object
2. **Records**
3. **Record list**
4. **Record Centric Approach:** Design objects around record types
5. **Relationships:** creates a link between fields in the two record type
6. **Record Links:** can help users to view relevant information that supports the record, but doesn’t display directly in it

---

## Query Record Type
- Expression Rule: ATF_getALL
```
a!queryRecordType(
  recordType: RecordType,
  fields: {},
  pagingInfo: a!pagingInfo(
    startIndex: 1,
    batchSize: 100
  )
).data
```

## Display Records
**From Interface Design mode**
- Add a read only grid to the canvas and select the Relate record type as the data source
  - create a rule input of ParentRecord Type(will need a default value so you can test)
      - the test default value should query the record type
      - set this as a default vaule for the rule input
      ```
        a!queryRecordType(
          recordType: 'recordType!TTA Routine',
          fields: {},
          pagingInfo: a!pagingInfo(
            startIndex: 1,
            batchSize: 1
          )
        ).data
      ```
- create a filter, using the filter records option
    - Field: routineId = Value: ri!record[ParentRecord.id]

**From Interface Expression Mode**
- Add a gridfield component
  - add the related record as the data using a!recordData()
    - recordType: child record type
    - filters: add a logical expression configuration using a!queryLogicalExpression()

```
      a!gridField(
        data: a!recordData(
          recordType: 'recordType!TTA RoutineExercise',
          filters: a!queryLogicalExpression(
            operator: "AND",
            filters: {
              a!queryFilter(
                field: recordType!TTA RoutineExercise.routineId,
                operator: "=",
                value: ri!record[recordType!TTA Routine.id]
              )
            },
            ignoreFiltersWithEmptyValues: true
          )
        )
      ).......
```