# SysID

System Identification is the process of empirically poking at a system through it's inputs and seeing how it reacts. It is useul for obtaining feedforward constants for nearly all frc mechanisms.
See [here](https://docs.wpilib.org/en/stable/docs/software/advanced-controls/system-identification/introduction.html) for the WPIlib documentation.

## Example
Suppose we want to command an elevator to move at a certain velocity. Our feedforward equation will be of the form:

$$V = sign(K_s) + K_g + K_v * (v) + K_a * (a)$$
* V :: output voltage (V) - voltage to send to the motor(s)
* K_s :: static friction constant (V) - The voltage required to overcome the mechanism's initial friction
* K_g :: gravity constant (V) - The voltage required to overcome the force of gravity, for the mechanism to maintain it's position
* K_v :: velocity constant (V/ m/s) - The ratio of voltage supplied to output velocity of the mechanism
* K_s :: acceleration constant (V/ m/s^2) - The ratio of voltage supplied to output acceleration of the mechanism

If we want to drive the elevator to a velocity $v$ and accleration $a$, this equation describes the voltage required to do so.

Tuning for K_s and K_g manually is simple enough. For K_s, simply put the mechanism at it's state of highest potential and slowly increase the voltage output until the mechanism moves.
For K_g, simply increase the voltage until the mechanism can overcome the force of gravity on it's own. (For some mechanisms like arms, this may depend on the state of the mechanism)

Tuning for K_v and K_a manually is more challenging, which is why sysID gives us a more streamlined procedure for obtaining these values.

## Recalc

For simpler but less accurate approximations for many FRC mechanisms, see [ReCalc](https://www.reca.lc/).

## Phoenix6

Phoenix6 has a sysID implementation which is much more performant than the
method recommended by WPILib. Using their provided procedures can mitigate the
impact of CAN latency, robot cycle time desync, and JVM garbage collection
desync.

See [here](https://v6.docs.ctr-electronics.com/en/2024/docs/api-reference/wpilib-integration/sysid-integration/index.html).

### Swerve

Examples of sysID application to obtaining phoenix6 swerve drivebase constants can be found inside the [Phoenix6-Examples](https://github.com/CrossTheRoadElec/Phoenix6-Examples/tree/main/java/SwerveWithPathPlanner) repo.

