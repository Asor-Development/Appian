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