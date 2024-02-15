


## Start Process vs Sub process
- triggers a second process from inside another

### Start Process Smart Service
- processes run asynchronously
- will execute on different engine
- will manage load on the system by spreading the newly started processes across all execution engines

### Sub Process
- processes can run asynchronously or synchronously
- execution will happen in the same engine as parent process
- asynchronously will not allow you to get an output variable
- synchronously will allow you to get an output variable