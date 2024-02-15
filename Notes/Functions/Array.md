

## `append(array, value)`
- append a structure or value to an array
- ex. If we have an editable grid and we need to add rows, we can use the append function to add a blank structure to the exsiting array

---

## `joinarray(array, separator)`
- concatenates the elements of an array together into one string and inserts a string separator between each element

---

## `where(array)`
- returns the indexes where the values in the input array are true
- useful for finding values in an array that meet a certain criterion
- useful for checking the value of a field in an array of CDT field values
- if all values are false and no default is specified, an empty set is returned

---

## `wherecontains(value, array)`
- return indexes of an array that match a user-defined value/values
- useful for finding which items in a CDT array have the same value for a field

---

## `index(data, index, default )`
- returns the data at a specified index if it is valid or else returns the default value
- can return the values of an array at the indexes you gathered with the wherecontains() function

---