# Robot Pools
- a collection of robots that run robotic tasks
- each robot is installed on individual host machines
- when a robotic task is triggered, it can use any robot in a robot pool to complete the work
- if a host machine is down, or a robot is unavailable, a different, available robot in the robot pool would complete the work
- create different robot pools to categorize robots for purpose, security and system access
- a single robot can belong to multiple robot pools
- a pool can be aprt of other pools
- If a robot pool is not added, the robotic task can still be configured but will not be able to debug or execute
**After creating a robot, you can add your robot to a robot pool. Simply create a Robot Pool design object in your application to get started.**
---


# Robot Pools
- a design object that enable you to group robots based on their unique roles and capabilities
- ensure that there is always a robot available and ready to handle any robotic task execution
- to categorize robots for purpose, security and system access
- a collection/group of robots, each installed on individual host machines, that run robotic tasks
- can deploy, import, and export robot pools in the same way as other Appian objects, which makes the deployment experience consistent and familiar
- can also be used to improve security, as access to sensitive data can be restricted to specific robot pools
- If a host machine is down, or a robot is unavailable, a different, available robot in the robot pool would complete the work


## Robot Pools: Robots
- each robot pool with multiple robots can handle multiple executions simultaneously
- you can only add robots that you have permission to view or initiate based on the robot's security

## Robot Pools: Robotic Task
- when you create or manage a robotic task, you get to choose the appropriate robot pool responsible for executing the task
- when a robotic task is triggered, it can use any robot in a robot pool to complete the work
- it is easy for you to move robotic tasks to different robot pools if you need to improve performance or quickly make adjustments
- If a robot pool is not added to a robotic task, it can still be configured but will not be able to debug or execute

## Robot Pools: Robot Pool Hierarchy
- a robot pool can have other robot pools within it, forming a hierarchy and keeping things organized
    -  Circular membership is not allowed, meaning a pool can't be a member of itself or any other pool in its hierarchy
______________________________________________________________________________________________________

# Create A Robot Pool: Design Object
- give it a name and description
- Appian creates the robot pool and you're brought to the robot pool page where you can add robots or other robot pools

## Add or remove robot pool members
- open the robot pool page
- **Add members:**
    - Click the Add Members button to open the robot pool members dialog
    Enter the name of the robot(s) and robot pool(s) you want to add then click ADD. You are brought back to the robot pool page and the robot(s) or robot pool(s) you added display in the list.
**After adding the robot to a robot pool, it is time to create a [robotic task](./RoboticTasks.md).**