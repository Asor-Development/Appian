# Dictionary

- most common
- each value is tied to a specific key
- the key is typically a descriptive word of what the value represents
- `{key1: "value1", key2: "value2"}`
- to pull a specific value you can use either dot notation or the `index()` function
    - `index({key1: "value1", key2: "value2"}, key)`
    - `{key1: "value1", key2: "value2"}.key`
    - the `index()` function is preferred over dot notation because it is more reliable
- when data is returned from a dictionary the data type is any type, to find the underlying data type use map and `map()` function