# `load()` and `with()` functions are deprecated and replaced by a!localVariables()
- Load() calculates local variables value only first time when the expression is evaluated
- With() re-calculates local variable's value when the expression is reevaluated
---
# `load()` Function
- Lets you define local variables within an expression for an interface and evaluate the expression with the new variables, then re-evaluate the function with the local variables' values from the previous evaluation
- can define multiple local variable
- can save the data into a variable which is defined inside load()
- Variables defined in load() instantiate for only once
- forcefully you can dynamically change the value of the variables defined on load() as well
- consistent values should be maintained in the variables defined in load() 
- `a!localVariables()` does everything `load()` does but with additional refresh options that may drastically simplify your design

## `with()` Function
- lets you define local variables within a function and evaluate the expression with the new variables
- can define multiple local variable
- you can't perform save operation over the variables which are defined inside with()
- variables defined in with() will be evaluated for each interaction on form
- maintain those variables in with() which are expected to change its value based on given input
-  `a!localVariables()` does everything `with() `does but with additional refresh options that may drastically improve the performance of your design


 However .