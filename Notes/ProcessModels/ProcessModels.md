
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
- configure alert and data management settings
- limited number of node
- similar functionalities are create in a single process and that process is used as a sub process for a number of process models
- give proper security setting to users
- use proper annotations, to show what the process models is for and what it does
- remove unused PV