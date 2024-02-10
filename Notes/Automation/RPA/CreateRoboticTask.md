# Create Robotic Task
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

2. **Create A Robotic Task:** will tell the robot what work to complete