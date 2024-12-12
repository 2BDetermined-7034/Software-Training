# FRC Driverstation
Frc driverstation is the application which sends packets between the laptop and the robot. It is responsible for enabling/disabling, 
triggering autonomous/practice conditions, handling controller inputs; and logging important debug information like battery voltage, CAN utilization, radio uptime, etc. 

Use this for everything, it will be a short one. 
https://docs.wpilib.org/en/stable/docs/software/driverstation/driver-station.html

### Best Shortcuts
F1 - Force a Joystick refresh.

use the: key [ and the: key ] and the: key \ - Enable the robot (the 3 keys above Enter on most keyboards)

Enter - Disable the Robot

Space - Emergency Stop the robot. After an emergency stop is triggered the roboRIO will need to be rebooted before the robot can be enabled again.


### Setup
Click the gear symbol on the left.
Make sure that the team number is entered correctly.

### Status
In the middle of the screen you can see the current status.
Check  the team number, the battery voltage, all 3 indicators, and that the status message at the bottom.

### Operation
You can see the operation tab by clicking on the steering wheel on the left.

The robot modes are: Teleop, runs the teleop code; Automous, runs auto code; Practice, runs as if in a match; And test, runs test code.

You can Enable and Disable the robot from here.

You can see the time elapsed since the robot was enabled.

You can see the drain on the battery and CPU.

You can change window mode and the team station.

