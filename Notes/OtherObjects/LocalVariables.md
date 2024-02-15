# [Local Variales](https://docs.appian.com/suite/help/23.3/Local_Variables.html#configuring-refresh-behavior)
-  Local variables are only available within the context of a particular expression and can only be accessed within the function that defines them
- variables are considered dependencies even if they are only used within a part of the expression that isn't evaluated
- defined within the `a!localvariable()` function
    - the first parameters are reserved for the name and value of the variables
    - type is determined by the value
    - the last parameter is reserved for the evaluation of the variables
    ![Local Varables](../images/localvariables.png)
- when querying data you might want to query the database once the store it in a local variable and reference that variable when needed, if not then you would be querying the data every time you need it(performace)
- most local variables can be updated through a `saveInto` parameter
- some local variable configurations can make that variable an invalid save target
- `load()` and `with()` functions are deprecated and replaced by a!localVariables()
    - Load() calculates local variables value only first time when the expression is evaluated and With() re-calculates local variable's value when the expression is reevaluated
---

## Default Refresh Behavior for all local variables
- **refresh when a referenced variable in the value configuration changes**
    ![Local Varables Refresh](../images/localvariablesrefresh.png)
    - when `borrowDate` changes `returnDate` will automatically update by seven days at the same time
- **Never refresh:** variables with no dependencies will never refresh
- **Referencing specific fields within a variable:**
    - if a local variable depends on a specific field within another variable, it will only refresh when that field is updated
    - applies for both dot indexing and bracket indexing
    - also work for array indexing, but if you need to use the index function to provide a default value, then you need to place the index function in an intermediate local variable to achieve the same behavior
- you can still save into variales that can be updated automatically
- local variables that are used within interfaces can refresh their values under a variety of conditions
- you can change these refresh behaviors using the `a!refreshVariable()` function, only available within an interface

---
## Disable Default Refresh Behavior: `a!refreshVariable()`
- allow you to modify default refresh behavior 5 ways
- gives you control over what you want to use to trigger an update
    - can be a reference or specific variable, timer, user interaction or record action

    ### 1. `a!refreshVariable()`: `refreshOnReferencedVarChange` 
    - set the `refreshOnReferencedVarChange` parameter of the `a!refreshVariable` function to `false`
        - if you want to make a copy of a variable for later comparison
        - if you simply don't want something to be calculated each time a variable it depends on changes
    ![Local Varables Disable Refresh](../images/localvariablesrefreshdisabled.png)
    - `a!refreshVariable(value: local!fullName)` here fullName is the value when its created
    - if the users changes either field it will only update that field
    - if the user changes the value in the Full Name text field only `local!fullName` will change not `local!preferredName`
    - if the user changes the value in the Preferred Name text field only `local!preferredName` will change not `local!fullName`
    -----
    ### 2. `a!refreshVariable()`: `refreshOnVarChange`
    - refresh a local variable based on when a specific variable not refrenced in the value changes 
    - set the `refreshOnVarChange`  parameter of the `a!refreshVariable` function to the variable you want it to change based on

    ![Local Varables Disable Refresh](../images/localvariablesrefresh2.png)
    - everytime the `local!username` changes, the `local!usernameEditedTimestamp` will change

    ---

    ### 3. `a!refreshVariable()`: `refreshInterval`
    - refresh automatically on a timer
    - set the `refreshInterval`  parameter of the `a!refreshVariable` function to the time you want it to changed based on


    - [More](https://docs.appian.com/suite/help/23.4/Local_Variables.html#configuring-refresh-behavior)
    ---

    ### 4. `a!refreshVariable()`: `refreshAlways`
    - Refresh the data after each user interaction and each interval refresh
    - trigger refresh based on user interaction
    - set the `refreshAlways` parameter of the `a!refreshVariable` function to `true`
    - will refresh the variables whenever the user interacts with any of the interface components
    - will refresh on every interaction regardless of whether or not the dependencies change

    ### 5. `a!refreshVariable()`: `refreshAfter`
    - Refresh the data each time a record action dialog is submitted
---




## Summary
-  Local variables are only available within the context of a particular expression and can only be accessed within the function that defines them
- are defined in the `a!localVariables()`, with or without an initial value
- local variables that do not have an initial value are of type Null, this can often cause errors when trying to pass the local variable to a function, so you may need to cast it to the expected type
- you can use other types of variables as values, this creates a dependency between the two variables and ensures that the referenced variable is always evaluated first
- To keep your data up-to-date, you can configure a combination of five different types of refresh behavior in your interfaces using     `a!refreshVariable()`
    - allow you to modify default refresh behavior
    - gives you control over what you want to use to trigger an update
    - can be a reference or specific variable, timer, user interaction or record action
---
[load() and with() Functions]()




---