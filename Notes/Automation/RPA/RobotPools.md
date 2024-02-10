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