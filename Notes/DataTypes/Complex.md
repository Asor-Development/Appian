# Complex System Data Types
- structure of predefined fields
- cannot be modified
- structure consist of pre-defined fields that are used by components within Appian
- if you need to transform a set of data so it is reconized as a complex data type, you might need to used the `cast()` function
- dataSubset, EntityData etc...
    - DataSubset: holds the data returned by a query, represents the structure of the data returned by a query, if data needs to be identified as a DataSubset you can use the `todatasubset()` function

- **[Arrays](./Array.md):** collection of data tha relates to each other in some way

###### Map
- map data type and `map()` function allow us to know the underlying data type of data sets
- `a!map(key1: "value1", key2: "value2").ke1`
- avoids conversions/casting
---