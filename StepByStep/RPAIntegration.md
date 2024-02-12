# Create RPA Integration
- You will need a 
    - WebAPI key: required for Appian RPA to communicate with your application
    - Appian RPA Connected System
    - Integration Design Object
---

## Craete Connected System
1. Create Web API Key 
- an API key is created through the Admin Console from the Web API Authentication tab
- add it to a service account
- add the service account to the administrators group
    - ensure the WebAPI has access to the objects needed to trigger a robotic task
- copy the API key to add it to the connected system
2. Create an Appian RPA Connected System
    - choose Appian RPA
    - paste the generated API key into the configuration
## Create Integration
1. Create New Integration
    - Use the created Appian RPA Connected System
    - choose **Execute Robotic Task**
    - Configure Integration
        - **Robotic Task:** use the dropdown to choose the robotic task that the integration will trigger
            - service account needs to be part of the application administrators group for the robotic task to be visible in the dropdown
        - Configure Description and Priority as needed
        - create rule inputs and map them to the appropriate parameters
            - the rule inputs should match the inputs for the robotic task
            - update the value for the rule inputs in the Parameters section `ri!ruleInputName`
**Once you have your integration configured you can now update/create the process model**