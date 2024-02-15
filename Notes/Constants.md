# Constants


## Environment Specific
- when we create a CDT we have an option to create an Environment Specific constant
    - will require different environments to have different values for this constant
- prevents unintentional changes to an environment's value for this constant
- the value of an environment specific constant is not updated on import unless set via an import customization file
- Ex. when deploying you have to change the value during deployment via the import customization file

## UUIDs
- a UUID is automatically generated for every object, this UUID will remain the same from one environment to another
    - you can have two different kinds of object with the same name but the UUID will be different

## toString vs touniformString ???
- to string will join all into one string, creating a text string
- to uniform string will allow you to add a delimiter that each item will be separated by in the string

## Integration
- is used to 
## Web API
## Connected System