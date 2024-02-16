# Node Inputs
- is modified as part of the node
- you can save the results from the input in the SaveInto parameter
**Node Inputs and Process Variables**
- to pass data into a node input a value must be provided
- node inputs can be mapped to process variables or they can be constants, literal values, or an expression to be evaluated
- node inputs are mapped to process variables on either the Data Tab or the Setup tab of each activity or smart service
- you can specify a default value for the node input by using the Value field in the Node Inputs dialog, when the process variable you are mapping doesn't currently have a value

### Creating ACPs: Node Inputs
1. Right Click node and click the DATA tab then INPUT tab
    - node inputs/outputs are mapped to PVs on the Data Tab or Setup Tab of each activity or smart service
2. Under Node Inputs Click New Input and Configure
    - **Name:** name of ACP
    - **Type:**
    - **Value:** the process variable you want to use to pass data to the node input
    - **SaveInto:** the PV that will store the value of the ACp if needed