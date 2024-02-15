
- [Muti-Node Instances](./MNI.md):Execute any node mutiple times in a single process flow


## Ways to Start a Process
- you can start a process from an interface, tempo, site, portal, outside of Appian, automatically or from another process


## Activity Chaining
- when the same user need to complete a number or user input task one after the other
- if activity chaining is enabled after the user submits one task or form the next one will be displayed to the user
- if no activity chaining is enable then the second task will appear in the User's Task Tab in Tempo
- should use no more than 50 nodes or 5 seconds between attended activities

## Archiving
- if you do not need the instance in Appian you can just use the default 7 day archival, and it will no longer be avaliable in the monitoring tab
    - you can change it to 1 or 3 days depending on your requirements


## Errors in a process model
- you can set alerts to send alert messages to some person or groups, users do not always report issues
- you can also check for errors in the Health Check


## Process Model Best Practices
- give PM a Dynamic Display Name
- use the alert tab to assigns alerts to proper groups
- use data management tab to manage process instances(parent 1 day, sub processes 0 day)
- limited number of node
- similar functionalities are create in a single process and that process is used as a sub process for a number of process models
- give proper security setting to users
- use proper annotations, to show what the process models is for and what it does
- remove unused PV
- configure 30 nodes at most, there can be a high memory cousumption issue if there are more than 30 nodes
- if more than 30 nodes are required it should be broken up into sub processes
- user input task should also have a dynamic Task diaply name
- configure proper swim lanes
- use activity chaining to allow navigation from one task to the next without leaving the current screen, for tasks that need to be completed by the same user
- use at least one terminate event to stop all process flows for each process model(configure in the end node results tab)
- business users should have at least initiator access, so they can start the process