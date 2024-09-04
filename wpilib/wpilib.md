### WPIlib training
This document will provide resources for understanding how to perform basic operations of wpilib including creating a robot project, the fundamentals of command based programming, spinning motors, creating a drivebase, and running code on the robot
We will only cover basic operations because there are countless useful wpilib objects and you will have to do research through the docs to find the  ones you need to use to accomplish your robot programming goals. 
I recommend following these resources in order
Tests are required and will follow the same requirement from the last chapter of 80% unless otherwise noted. 

## Command Based Programming
The specific programming paradigm we use to organize our robot projects.

1. [What is Command Based Programming](https://docs.wpilib.org/en/stable/docs/software/commandbased/what-is-command-based.html)
2. [Commands]9https://docs.wpilib.org/en/stable/docs/software/commandbased/commands.html)
3. [Subsystems](https://docs.wpilib.org/en/stable/docs/software/commandbased/subsystems.html)
4. Test What are commands and subsystems - PlaceHolder
5. [Structuring a Command Based Project](https://docs.wpilib.org/en/stable/docs/software/commandbased/structuring-command-based-project.html)
6. [Organizing a Command Based Project](https://docs.wpilib.org/en/stable/docs/software/commandbased/organizing-command-based.html)
7. [The Command Schedular](https://docs.wpilib.org/en/stable/docs/software/commandbased/command-scheduler.html)
8. Test RobotContainer structure, best practice organization - Placeholder

## Spin a motor with commands
Excercise in using command based programming to spin a motor - Placeholder

## Tank Drivebase Excercise
Create a tank drive using Neo brushless motors - Placeholder

## Telemetry
Section for logging information from the robot through the networktables server. This is very uesful and a prerequisite to achieving anything more complex in wpilib.
1. [NetworkTables](https://docs.wpilib.org/en/stable/docs/software/networktables/index.html) - More in depth, and faster in situations where performance matters, but for most situations you can use [Shuffleboard's java api.](https://docs.wpilib.org/en/stable/docs/software/dashboards/shuffleboard/getting-started/shuffleboard-displaying-data.html)

### Dashboards
All of these are useable but the default all purpose dashboard is now AdvantageScope. Glass is more powerful and is the expected interface for other official wpilib tools like System Identification and Robot Simulations, but AdvantageScope is simply more convenient. Others like Shuffleboard are extremely customizable and many teams have their own color themes, including us with our shuffleboard theme repo. It's recommended to pick one of these as your default network tables veiwer but know how to navigate all of these in a pinch.
1. [AdvantageScope](https://docs.wpilib.org/en/stable/docs/software/dashboards/advantagescope.html)
2. [ShuffleBoard](https://docs.wpilib.org/en/stable/docs/software/dashboards/shuffleboard/getting-started/shuffleboard-tour.html)
3. [SmartDashBoard](https://docs.wpilib.org/en/stable/docs/software/dashboards/smartdashboard/index.html)
4. [Glass](https://docs.wpilib.org/en/stable/docs/software/dashboards/glass/index.html)
5. 
