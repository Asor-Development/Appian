# Constants
- used when you have data that will not change or will rarely change
- can be referenced in an expression
- if you need to change the value you only need to change the contstant and it will change in everyplace that you have used the constant
- uses the prefix `cons!`
- contains single values, lists of values and pointers to other objects
- do not contain expression
- a single location where a value lives
- can create constants that point to the groups and folders
<!-- - constants are auto generated when you create a record action -->


## Environment Specific
- when we create a CDT we have an option to create an Environment Specific constant
    - will require different environments to have different values for this constant
- prevents unintentional changes to an environment's value for this constant
- the value of an environment specific constant is not updated on import unless set via an import customization file
- Ex. when deploying you have to change the value during deployment via the import customization file
