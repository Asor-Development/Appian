


## Escalation and Exception
- both used in process models
- **Escalation:**
    - when a task or process node is delayed for some reason
    - can configure using a time event, change the priority, reassign task, send a alert or message
    - Ex. if you have a task that has not been completed for a certain amount of time you can send a reminder or alert to the user or group to complete the task
- **Exception:**
    - Ex. if a user starts a process and for some reason the process never get completed
    - can terminate the process, or take an alternative workflow based on some condition
    - can be configured based on time event, rule event or receive message event
    - can be configured on any node that is not and event or gateway node