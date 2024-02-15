# Questions
1. What is an environment specific constant? [Answer]()

## UUIDs
- a UUID is automatically generated for every object, this UUID will remain the same from one environment to another
    - you can have two different kinds of object with the same name but the UUID will be different

## toString vs touniformString ???
- to string will join all into one string, creating a text string
- to uniform string will allow you to add a delimiter that each item will be separated by in the string

## Integration
- allows Appian to call or use external systems
## Web API
- expose Appian data and services to external systems
## Connected System
- stores authentication and connection information so you can connect to external integrations and data sources

## Escalation and Exception
- both used in process models
- escalation
    - when a task or process node is delayed for some reason
    - can configure using a time event, change the priority, reassign task, send a alert or message
    - Ex. if you have a task that has not been completed for a certain amount of time you can send a reminder or alert to the user or group to complete the task
- exception
    - Ex. if a user starts a process and for some reason the process never get completed
    - can terminate the process, or take an alternative workflow based on some condition
    - can be configured based on time event, rule event or receive message event
    - can be configured on any node that is not and event or gateway node


## Deployment
- Dev to test:compare and deploy feature
- Deploy to production: export manually

## Process Model 
#### Archive
- if you do not need the instance in Appian you can just use the default 7 day archival, and it will no longer be avaliable in the monitoring tab
    - you can change it to 1 or 3 days depending on your requirements

- How to check errors in a process model
    - you can set alerts to send alert messages to some person or groups, users do not always report issues
    - you can also check for errors in the Health Check

- Ways to Start a Process
    - you can start a process from an interface, tempo, site, portal, outside of Appian, automatically or from another process
- Start Process Smart Service
    - triggers a second process from inside another
    - processes run asynchronously
    - will manage load on the system by spreading the newly started processes across all execution engines
- Sub Process
    - triggers a second process from inside another
    - processes can run asynchronously or synchronously
    - execution will happen in the same engine as parent process
    - asynchronously will not allow you to get an output variable
    - synchronously will allow you to get an output variable
- Gateways
    - XOR: like a if else condition, with mutiple outgoing paths that allows only one path to be executed
    - OR: like if condition, with mutiple outgoing paths that allow mutiple outgoing paths to be excuted when the conditions are true
    - AND: like fork and join, it will wait for all the incoming paths to reach the node, then execute all outgoing paths at the same time
        - does not require any configuration
    - COMPLEX: combination of all the gateways
- Activity Chaining
    - when the same user need to complete a number or user input task one after the other
    - if activity chaining is enabled after the user submits one task or form the next one will be displayed to the user
    - if no activity chaining is enable then the second task will appear in the User's Task Tab in Tempo
    - should use no more than 50 nodes or 5 seconds between attended activities


---
## BP
Process Model
    - give PM a Dynamic Display Name
    - configure alert and data management settings
    - limited number of node
    - similar functionalities are create in a single process and that process is used as a sub process for a number of process models
    - give proper security setting to users
    - use proper annotations, to show what the process models is for and what it does
    - remove unused PV

Interface
    - whne using complex logic, comments should be used to communicate to other developers what it is doing, or give the Jira ID
    - when querying data create an expression rule and call it from the interface, that way it can be more dynamic or generic 