# Set Up the RPA Robot
1. Navigate to the Operations Console(located in the waffle menu in the upper right-hand corner)
    - Click Create
    - Add Robot Details:
        - **Name:** Editable name for the robot that is shown throughout Appian.
        - **Operating system:** Choose the host machine's operating system: Windows, Linux, or Mac.
        - **JRE path (./%JAVA_HOME%):** Optional field to specify where Java is installed on the host machine.
        - (Windows host machines only) Optionally, choose to Allow Appian to Sign In by checking the Enable automatic sign in box
    - Configure Robot Security:
        - Assign user or group security role maps to the robot
    - Manage Connection: connects the robot to a host machine
        - If your organization uses robot keys, copy the robot key now. You will not have another chance to view it.
        - Verify your host machine is ready for robot installation and download the robot installer. If you're using a physical host machine, you'll download the robot and launch it now. If you're using a virtual host machine, you can complete this step later

**Follow the onscreen instructions to download and run the robot on your host machine, when finished, click Done. Your robot should now appear Online in the Operations Console.**
**After creating a robot, you can add your robot to a robot pool. Simply create a Robot Pool design object in your application to get started.**
---

## Add Robot to robot Pool
1. From Appian Designer select New and Robot Pool
    - name the pool and click Create and Save
2. From within the pool
    - Click Add Memebers
    - Under Robots To Add, search for robot and click Add