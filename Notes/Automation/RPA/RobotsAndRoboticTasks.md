# Robots and Robotic Tasks
**You must Configure a Robot before you create a robotic task**


## Configure Robot
1. **Configure Robot:** You need a robot to do the work on a local or virtual machine
    - Go to the Operations Console
    - Click create and follow the prompts
    - Provide a name for your robot
    - Choose the operating system the agent will be installed on 
    - the JRE Path and Allow Appian to Sign In are optional and can be configured as needed
        - Read more about these configuration options in Appian Documentation
    - Set security on your robot using rolemaps
    - Configure which user groups should have Administrator, Editor and Viewer access to the robot
        - can also configure Deny
        - Read more about these permission levels in Appian Documentation
    - Download and run the agent
        - Once the agent runs on the host machine, its status is Online, and it can communicate with the orchestration server
    - After creating a robot, you can add your robot to a robot pool by creating a Robot Pool design object
**After creating a robot and adding it to a robot pool, it is time to create a robotic task.**

## Create A Robotic Task
2. **Create A Robotic Task:** will tell the robot what work to complete
    - Create a Robotic Task Design Object
    - Configure robotic task actions, screen consist of four tabs: 
        - **Edit:** to design the robotic task by dragging and dropping components from the Palette on the left to one of the sections in the middle of the screen
            - use robotic task variables to pass data between actions and other design objects
            - Setup, Main and Clean up are the default sections
        - **General Information:**
        - **Run-Time Settings:**
        - **Technical Information:**

### Edit Tab
- **Robotic task execution:**
    - starts at the top, in the **Setup section**
        - should contain tasks that prepare the host machine, such as opening a browser or verifying that folders to be used for downloads don't have unnecessary documents
    - then executes actions through the **Main section**
        - use the Task Recorder to record browser actions
        - you can map variables during the recording, or once it has been saved to your robotic task
        - save captured attributes as a variable, which can be used to pass the data into other desig objects
        - You can edit the actions in the Task Recorder or in the Setup, Main, or Clean up section
        - After saving the recording using a name of your choosing, it’s saved as an action group in the Main section
    - and finally through the **Clean up section**
        - configure the steps the robotic task should take when it's complete, such as closing programs it opened
        - always runs at the end of your robotic task, whether it succeeds or fails
        - use the Clean up section to return the host machine to its original state
- **Action Groups:**
    - useful for organizing individual actions that together complete a task
    - can rename each Action Group to something meaningful for your robotic task
    - can easily move the Action Groups when you need to reorder the sequence of actions to execute
- **Configure Actions:**
    - the Action Configuration panel appears on the right, beneath the Variables panel, as you add actions to your robotic task
    - select an action in one of the sections, to display its configuration settings in the Action Configuration panel
    - you need to configure these fields to make the action work in your task

### General Information Tab
- new RPA developer should focus on the Description and the Robot Pool fields
- Permission Tags are used to give the robotic task access to credentials and queues in the Appian RPA console

### Technical Information Tab
- the Select Support File section is where you place files the robotic task needs during execution, such as web browser drivers.
- if your robotic task uses the Internet Explorer or Opera web browser, the web driver support file must be added to the Support Files folder
- the version of the driver must match the version of the web browser on the host machine
- See the Appian documentation for details on adding support files, including browser drivers
**Appian can update web drivers automatically when the robotic task uses Chrome, Firefox, or Edge. Instead of having to manually download and add web drivers to your support files, Appian can automatically maintain Selenium web drivers for you. This option is off by default**
- **To allow Appian to automatically provide web drivers:**
    1. Go to the Settings tab in the Appian RPA console.
    2. On the Configuration tab, go to Security policies.
    3. Select Allow Appian to provide selenium web drivers.
    4. Click Save security policies.


https://academy.appian.com/#/online-course-player/a11e15e0-bea2-4218-9ace-9bd2903a1299


---

### Debugging Robotic Tasks
**Appian RPA's native debugging tool helps you test and confirm configurations for individual actions in the workflow, so you can focus your efforts on fixing what might be going wrong**
- can debug a robotic task directly from the screen where you designed it
     - click Test located above Setup
     - you can provide test values for your parameterized variables to use during testing 
- buttons used to debug the task are located in the top right corner toolbar
- you can test each action in the task by clicking the Next Action button. Click this button after each action is completed, and displays a large “Success” message 
- a green checkmark displayed beside each successfully completed action
- when the debug tool has finished testing all the actions, the debug toolbar disappears

#### Errors
- When the debug tool does encounter a problem, it will highlight in red the problematic step and display a red caution symbol
- you can click the **Execution Log** tab to look for the error
    -  if you want to check the configuration settings for the step, click End Execution, then return to your robotic task
- You can:
    - **adjust the robotic task variables** during execution, by clicking on the task variable and update the value when needed before proceeding to the next action
        - will only change the variable during the debug instance and will not change the robotic task itself
    - **set breakpoints** where you want the execution to pause so you can perform an assessment
        - use the Add/remove breakpoint option to pause the task so you can check that a variable was properly captured.
    - **disable actions**, which will be skipped during the debugging execution
    - **run a task from a specific action** use the Run from action to isolate an action to check if it’s executing properly
- To debug a robotic task, line-by-line, select Execute, the Debugging checkbox, then use the Next Action button to step through each action of your robotic task
- The Execution log tab provides detailed information
- While debugging, you can re-run the task execution from the top, by clicking the blue circle icon in the top right. This refreshes the screen and starts debugging from the top
**The debugging tool will open in the Appian RPA console as a separate tab, whne you are done you can close this tab and return to the robotic task design object**


---
### [Permission Tags](https://docs.appian.com/suite/help/23.3/rpa-9.3/security-rpa.html#permission-tags)
- Permission tags are used to:
  - Allow users to access robots
  - Define which queues a robotic task can act on
  - Define which credentials can be used with a robotic task
  - Different users can access the same robot, queue, or credential no matter what their role is – they just need to share a tag with that component
  - You can create permission tags in the robotic task general tab
#### Add permission tags to user
- Appian RPA --> Users, locate the user --> Actions