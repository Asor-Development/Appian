# Interfaces


## Solutions
#### An Interface with rule inputs cannot be saved as a site page
1. Replace the rule inputs with local variables
2. If you use this interface in other spots as well, wrap it into a new interface that creates the required local variables and passes it to the rule inputs. Then use the new interface in the site.



## Interface Best Practice
- when using complex logic, comments should be used to communicate to other developers what it is doing, or give the Jira ID
- when querying data create an expression rule and call it from the interface, that way it can be more dynamic or generic 


---
### Validation Groups
validationGroup (Text): When present, this field is only validated when a button in the same validation group is pressed