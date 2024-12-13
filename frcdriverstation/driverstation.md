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

You can also reboot the roboRIO or restart the robot code.


### Diagnostics
The diagnostics tab located right under the operation tab and is used to diagnose issues with the robot.

You can find the DS version number, roboRIO image version, WIPlib version, CAN device versions, and roboRIO memory stats.

### Setup
Click the gear symbol on the left.
Make sure that the team number is entered correctly.

You can find and edit the team number, dashboard type, game data, practice mode timing, and audio control in this tab.

### USB
Under the setup you will find the USB tab.

You can find the list of all USB devices connected.

At the bottom there is the rescan button to find new USB devices.

You can find device indicators to see the state of the buttons, axes, and joystick.

You can lock devices to specific USB slots.

### Power
The last tab is the power tab. You can see all information on the power and if certain parts such as the roboRIO are browning out.









