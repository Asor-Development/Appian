## RPA Architecture
- organizations can used Appian RPA to automate the work of their employees, freeing them to do more interesting, cognitive work
---
### Appian RPA Components
- **In Appian Cloud**
    - **Connected Systems and Integrations** allow an Appian process to trigger and execute robotic tasks
    - during task execution the **Orchestration Server** communicates with each robot about which actions to complete next
        - talks to the robot agents located on the host machines
- **From Client Infrastructure**
    - **Robots** execute robotic tasks on host machines using agents
        - an agent can be your computer or a remote desktop
        - after you create a robot, you then download and run the agent on the host machine
        - each robot is secured separately directly from the Operations Console
            - users must be an Administrator or an Editor of the robot
        - being a viewer allows the user to see the robot in the Operations Console and use the robot in Appian Designer
---

## Appian RPA console
- can be accessed from the Appian Designer navigation menu
- was the primary way to interact with RPA including creating robots and robotic tasks(before 23.3)
- has been simplified with the Operations Console and a new design object for robotic tasks
- developers can use the Appian RPA console to schedule events and set alerts
- **Dashboard :**
    - displays by default, provides glance at status of all robotic tasks(it is recommended to use the Operations Console to view the progress of your robotic tasks)
- **Credentials:**
    - if the robotic task will need to access an application that requires login credentials, you can add them on the Credentials page
    - enables you to securely store the password so it isn't available in plain text. Add a shared permission tag for the credential and the robotic task
- **Workflow Libraries:**
    - a set of code and classes designed to be reused both within a robotic task and across multiple robotic tasks
    - create custom low-code methods for your robotic tasks
    - can import and export libraries

## Operations Console
- can be accessed from the Appian Designer navigation menu
- where authorized users can create, manage and view robots used in the environment
    - any user who is added to the Designer role, System Administrator role, or a member of the RPA Operations Managers system group has access to the Operations Console
    - Users need to be at least an Editor to manage a robot in the Operations Console
- other users can monitor running, queued or executed robotic tasks for any robot they have access to
- **Robot Management Screen:**
    - displays all robots in the environment, you would only see robots that you have access to
- **Robot Details:** click into a robot
    - users will be able to manage robot configurations and view currently running, queued and executed robotic tasks
    - users need to be at least a Viewer of the robotic task design object to see it in this view

---


### Creating Robots
- you can create a robot from the operations console or from Appian Designer
---

### Summary
- part of the Automation Suite
- has a set of components that work together to execute robotic tasks
    - Connected Systems, Integrations and Robots
- Operations Console is used to create, manage and view robots
- robotic tasks are design objects that can be secured using rolemaps like Viewer, Editor and Administrator