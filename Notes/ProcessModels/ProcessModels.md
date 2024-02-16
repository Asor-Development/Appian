# Process Models
**Process models are a way to graphically describe business processes. In Appian process models are not just the starting point for building your process, it is the process. Appian translates your business workflows to executable processes automatically**
- the process modeler is used to diagram business process using standard business process model and notation symbols
- has drag and drop activities that developers can use to create a workflow for automated task to execute specialized business services based on the user input 
- process model are not static
- **Processes:** enable performing activities that capture and modify data
 - query data, assign tasks, perform calculations on data, send email, generate document
- **Naming:** `AX Add Vehicle Form` Application prefix and spaces between words
- **Security:** process model do not inherit security from their folders
- **Actions:** each action and related action should be linked to a process model
    - drives actions perform in the application
    - actions are used when there is no specific record involed(add vehicle etc...)
    - related actions are preform on specific records
    - a process model should be linked to each action and related action
    - document each action/related action, the record, and the process model
**To work on Process Models make sure you're a member of the Process Model Creators system group**

---

## The Process Modeler Views
- **Analysis View:** can be used during planning to draw a simple process model
    - used to create a high level view of the process, it is recommened that you keep this diagram as a separate object
    - can reference this process model when you are creating the process model in designer view
    - can include annotations
- **Designer View:** where  you crate a working process model with functionality
---

## Process Model compoenets/nodes
- test and debug each node after it is added to the process model
- SHIFT will automatically toggle your pointer to the connector tool(can also use the Connect 
 icon to connect the nodes)

---

## Major elements used to build a process model
- **paleltte:** where you select and search for nodes and smart services
- **Standard Nodes:** used to capture and process business data, and control processes
    - [More About Standard Nodes...]()     
- **Smart Services:** provide speicalized business services,these services complete specific tasks such as sending emails, or creating folders or calling integrations there are two types
    - [More About Smart Services...]()
- **canvans:** where you create and configure the process model
- **tool bar:** where you access process model tools and properties(process instances)
- **menu:** where you access additional tools and properties
---


## Documentation
**To preserve a record of your work select tools and generate documentation from the menu**
- creates a summary of the process model with information about the properties, diagram, nodes, and content 

## Hidden Variables
- variables that cannot be used in process reports, parent processes and hides it from process history
- useful when optimizing for memory efficiency
- Parameters cannot be hidden
- can still be seen when monitoring the process instance
- configure on the Process Model's Variables Tab
---

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
- **Look for reusablity:** are any steps repeated, think about creating a subprocess that can be called each time a process needs to complete these steps, this tends to be more efficient and reduces the memory footprint for the model


---
- [Muti-Node Instances](./MNI.md):Execute any node mutiple times in a single process flow


