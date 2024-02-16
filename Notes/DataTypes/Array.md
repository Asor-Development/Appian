# Arrays
- an ordered list of data items that relates to each other in some way and can be selected by indices
- indices start at 1
- can be empty or constructed with literal values, variables, or functions
    - items in a list that contain data queries may be evaluated in parallel to reduce the overall evaluation time
- only one-dimensional arrays can be specified
- nested arrays are flattened to a one-dimensional array.
    - **Example:** `{{1, 2}, {3, 4}} = {1, 2, 3, 4}`
- if you need a multi-dimensional arrays, create a [complex data type](./Complex.md)
---

## Accessing array items at an index
- to select one or more values from an array, use the index operator `[]` or `index()` function
    - `{100, 235, 345, 426, 534}[2]` returns 235
    - `{100, 235, 345, 426, 534}[{1, 2, 4}]` returns {100, 235, 426}
    - `index({100, 235, 345, 426, 534}, 5, 1)` returns 534
    - `index({100, 235, 345, 426, 534}, 7, 1000)` returns 1000
    - you can also return the value of a map field using the field name as the index argument... [more info](../Functions/Array.md#indexdata-index-default)
[More Array Functions](../Functions/Array.md)



- Check out the [Documentation](https://docs.appian.com/suite/help/23.4/parts-of-an-expression.html#arrays) for more

    