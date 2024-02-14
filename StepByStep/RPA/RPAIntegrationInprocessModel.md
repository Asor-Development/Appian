# In the process model, add and configure the smart service to run a robotic task
1. Add the  **Execute Robotic Task smart service** to the process model

2. Configure the smart service settings on the Setup tab
    - select the RPA integration
    - you can edit the integration here if you need to 
    - set retries, must be between 0 and 5 inclusive
3. Configure Additional Settings on the Data Tab
    -  the integration's inputs will automatically appear as node inputs on the Data tab
    - **Node Inputs:**
        - add the value property value
            - if you are using record types you can select the record field name
            - this will pass the value from the interface into the robotic task
    - **Node Outputs:** 
        - specfies whether and where to save the node outputs
        - the Variables parameter in the Output tab would be mapped to a process variable, this parameter uses the Map() data type
        - if you need to pass information from the robotic task to the rest of the process
            - click New Custom Output and name it
            - Expression: Click the Expression Editor button next to Expression and enter the following expression `ac!Variables.variablename`
            - Target: use the dropdown to select record field that correspones with the information coming forom the robotic task
