# Process Model Security
https://docs.appian.com/suite/help/23.4/process-model-object.html#security
- do not inherit security from their parent folders
- security must be set on each process model individually
- user must have at least Initiator permissions to start a process model
- when a process model is started by a record action, the user's process model permission is checked to enforce record action security
- security role map of a process model controls which users can see or modify it and its properties
- **Permission levels**
    - Viewer, Editor, Administrator, Initiator, Manager and Deny permissions