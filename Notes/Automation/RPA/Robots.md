# Robots and Robotic Tasks# Robots
- you can create a robot from the operations console or from Appian Designer
- you must Configure a Robot before you create a robotic task
    - robotic tasks are assigned to robots
- each robot is installed on individual host machines
- How to configure a robot [here](../../../StepByStep/SetUpRobot.md)
- after your robot is configured you can add it to a [robot pool](./RobotPools.md), then you can creat a [robotic task](./RoboticTasks.md)
- If a robot pool is not added, the robotic task can still be configured but will not be able to debug or execute
---

## Allow Appian to sign in
- before a robotic task starts, it may need to access your host machine and start a user session if one isn't already active
    - your business may restrict the privileges available to this user session
- can configure your robot to allow Appian to automatically sign into a virtual machine as any designated user (basic or administrator) in order to start a robotic task
- you won't need to keep user sessions active on virtual machines in case a robotic task needs to start
- Appian can start a session as needed for robots with Standby status
    - can also automatically sign out of the host machine if there are no more robotic tasks to run after the last execution
    - Configure this option to build more flexibility into your unattended automations
**Appian only supports Enable automatic sign in on Windows host machines**

## Security
**Security for robots consists of the following:**
- system groups that manage access to the Operations Console, the RPA console, and the ability to create robots
- security role maps that manage activities related to robots

### Robot security by system group
- Access the Operations Console and view the Robot Management page form the RPA Operations Manager and Designer
- can create a new robot from the RPA Operations Manager but not Designer

### Robot security by role 
**Starting from the Appian 23.4 release, newly created robots can only be secured using role maps.** 
- The security role map of a robot controls whether users can view or modify it and its properties
- Robots never inherit security
- certain actions can be completed for each permission level(admin, editor, viewer, deny) in a robot's security role map
    - [More...](https://docs.appian.com/suite/help/23.4/rpa-9.7/manage-robots.html#security)

---


## Configure Robot
1. **Configure Robot:** You need a robot to do the work on a local or virtual machine
    - Go to the Operations Console to create robots
    - Download and run the agent
        - Once the agent runs on the host machine, its status is Online, and it can communicate with the orchestration server
    - After creating a robot, you can add your robot to a robot pool by creating a Robot Pool design object
**After creating a robot and adding it to a robot pool, it is time to create a robotic task.**