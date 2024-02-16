# Activity Class Parameters(ACPs)
**Variables that are unique to a specific node, you can think of them like local variables for process nodes**
- act as containers to capture data that is specific to one node
- are both node inputs and node outputs
- only exist in the node
    - when a node completes the ACP value is no longer available, so ACP values should be stored in a process variable if they need to be used later in the process
- the data stored is used to perform some kind of activity
- You will not have the same ACPs on both the Input and Output Tab
- any data you want to be used by a process node needs to be mapped to a node input
- standard nodes do not have any Node Inputs by default
- many smart services have predefined node inputs
- [Node Inputs](./NodeInputs.md)
- [Node Outputs](./NodeOutputs.md)

**Node inputs and Outputs save at the same time so,you should not save into the same process variable in node inputs as you do in node outputs, because the value you intend to end the node with may be overwritten**
