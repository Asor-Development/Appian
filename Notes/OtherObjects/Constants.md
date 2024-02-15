# Constants


## Environment Specific
- when we create a CDT we have an option to create an Environment Specific constant
    - will require different environments to have different values for this constant
- prevents unintentional changes to an environment's value for this constant
- the value of an environment specific constant is not updated on import unless set via an import customization file
- Ex. when deploying you have to change the value during deployment via the import customization file
