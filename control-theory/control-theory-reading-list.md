# Control Theory Reading List

This article aims to be a list of resources presented in a reasonable order for learning all there is to know about relevant frc control theory with a distinction between classical and modern control theory. I recommend getting a grasp on classical control theory before starting on the modern control theory resources, and making a consideration on whether your project requirements would be better achieved by each type of control.


## Control Theory Textbook 
[controls-engineering-in-frc.pdf](controls-engineering-in-frc.pdf) - This textbook is the best resource for control theory in FRC and will be commonly referenced throughout this article.

## Pre Requisites
The math for control theory (especially modern control theory) can become mathematically dense with really quickly, it is recommended to get a grasp of the fundamentals of calculus and linear algebra before delving into this reading list. This will likely be the most daunting challenge of getting into advanced control theory, but it will also set you up extremely well for any math classes you take in the future from now to the undergraduate level. I hope to make these resources as accessible as possible. You do not need to use all of these resources, I recommend finding the one you prefer to learn with, first with calculus, then with linear algebra. Finally I recommend attempting a few practice problems on these topics, for now you will have to seek these out yourself but I will add some at a later date. 

### Videos

#### Calculus
* [3Blue1Brown Essence of Calculus (Videos 1-5, 8-10)](https://www.youtube.com/playlist?list=PLZHQObOWTQDMsr9K-rj53DwVRMYO3t5Yr)
* [Understand Calculus in 35 Minutes](https://www.youtube.com/watch?v=WsQQvHm4lSw)
* [Khan Academy Calculus Course](https://www.khanacademy.org/math/ap-calculus-ab)
* Textbook Chapter 4

#### Linear Algebra
* [3Blue1Brown Essence of Linear Algebra (Videos 1-12)](https://www.youtube.com/playlist?list=PLZHQObOWTQDPD3MizzM2xVFitgF8hE_ab)
* [Khan Academy Linear Algebra Course](https://www.khanacademy.org/math/linear-algebra)
* Textbook Chapter 5


## Classical Control Theory

### Textbook
* Chapter 1 - Fundamentals
* Chapter 2 - PID Controllers
* Chapter 3 - Actuator Saturation

### WPILib Controllers articles
* [Controllers Overview](https://docs.wpilib.org/en/stable/docs/software/advanced-controls/controllers/index.html)
* [PID Controllers](https://docs.wpilib.org/en/stable/docs/software/advanced-controls/controllers/pidcontroller.html)
* [Feedforward Controllers](https://docs.wpilib.org/en/stable/docs/software/advanced-controls/controllers/feedforward.html)
* [Combining Feedforward and Feedback](https://docs.wpilib.org/en/stable/docs/software/advanced-controls/controllers/combining-feedforward-feedback.html)
* [Trapezoidal Motion Profiles](https://docs.wpilib.org/en/stable/docs/software/advanced-controls/controllers/trapezoidal-profiles.html)
* [Profiled PID Controllers](https://docs.wpilib.org/en/stable/docs/software/advanced-controls/controllers/profiled-pidcontroller.html)


## Modern Control Theory
Using Modern Control Theory can be incredibly rewarding, but it is also significantly more challenging than using Classical Control Theory. I recommend using it if you feel confident in your calculus and linear algebra  skills, 

I recommend first reading the wpilib articles, then only the fundamental textbook chapters, and then only reading chapters relevant to your system.

### Textbook 
* Chapter 6 - State Space Control (Defining feature of modern control theory)
    * 6.1 - 6.8 Introduction, Stability, Augmentation
    * 6.9 - 6.11 System Specific Examples
* Chapter 7 - Discrete State Space Control (Turns continuous equations into discrete ones letting us run them on the robot)
    * 7.1 - 7.6 Discretization
    * 7.7 Linear Quadratic Regulators
    * 7.8 - 7.9 Computer Integration Methods
* Chapter 8 - Nonlinear Control (Ignore unless you are doing a nonlinear system, even then I recommend using linearization over implementing nonlinear control) 
* Chapter 9 - Stochastic Control Theory (You probably want to ignore this)
    * Deals with probability and uncertainty in system and sensor measurements, may be necessary to optimize complex systems for good control
* Chapter 10 - Pose Estimation (Estimating the system's state from sensor measurements, feel free to skip over)
* Chapter 11 - Dynamics (Reference Equations for common systems, read fully only if you want to derive them yourself)
* Chapter 12 - Newtonian Mechanics (Full Examples of Newtonian systems for reference)
* Chapter 13 - Lagrangian Mechanics (Advanced, full examples of lagrangian modelled systems)
* Chapter 14 - System Identification (Some systems have simpler procedures for implementing control)
* Chapters 15 - 17 - More Motion Profiling

### WPIlib Articles

* [State Space and Model Based Control](https://docs.wpilib.org/en/stable/docs/software/advanced-controls/state-space/index.html)
* [Introduction](https://docs.wpilib.org/en/stable/docs/software/advanced-controls/state-space/state-space-intro.html)
* [State Space Controller Walkthrough](https://docs.wpilib.org/en/stable/docs/software/advanced-controls/state-space/state-space-flywheel-walkthrough.html)
* [State Observers and Kalman Filters](https://docs.wpilib.org/en/stable/docs/software/advanced-controls/state-space/state-space-observers.html)
* [Pose Estimators](https://docs.wpilib.org/en/stable/docs/software/advanced-controls/state-space/state-space-pose-estimators.html)
* [Debugging State Space Controllers](https://docs.wpilib.org/en/stable/docs/software/advanced-controls/state-space/state-space-debugging.html)


