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