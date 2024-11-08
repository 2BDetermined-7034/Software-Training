# **YAGSL Configuration Template**

[Printable Version](https://docs.google.com/document/d/1DdoC7-qEt5No5Sxrqn3X73GpjlmOa_MJbDjQnnJ3lek/edit#heading=h.dcusnnql1bi2)

https://yagsl.gitbook.io/yagsl/configuring-yagsl/configuration

> [!NOTE]: When viewed from the top, make sure the sides of the wheel with the bevel gear are pointing to the **left***

### Swerve Orientation Diagram

![](https://lh7-us.googleusercontent.com/XirSC03wrK04N9SoedFGmggFNO8v5jQ94hBoevcuVoXEUsXl359jB1OAMyJD69ybzAbPO90OFj4lW84jSzxHppKkM6jhKjuBOIeotRY21oH3oJ5aP1XO5CAXGt_ojif7Q7_QI2BaYlc6s53j_tAMNHs){width=624 height=568}

### 

### Module Types

| <br /> | Model, Version, Etc |
| --- | --- |
| Motor | <br /> |
| Motor Controller | <br /> |
| Absolute Encoder | <br /> |
| IMU | <br /> |

### Build Specific Details

> [!NOTE]: This template assumes a **square** swervedrive configuration, specifying positions using*\* [robot relative axes](https://docs.wpilib.org/en/stable/docs/software/basic-programming/coordinate-system.html).\*\*\*

#### Module Positions

| Module | X (in) | Y (in) |
| --- | --- | --- |
| Front Left | \+____ (put distance here) | \+____ |
| Front Right | \+____ | \-\~ |
| Back Left | \-\~ | \+\~ |
| Back Right | \-\~ | \-\~ |

---

#### 

#### Module Gearing

Calculate the drive/angle conversion factors

* Drive Motor Conversion Factor (meters/rotation) = (PI \* WHEEL DIAMETER IN METERS) / (GEAR RATIO \* ENCODER RESOLUTION)
* Angle Motor Conversion Factor (degrees/rotation) = 360 / (GEAR RATIO \* ENCODER RESOLUTION)

| <br /> | Wheel Diameter (m) | Gear Ratio | Encoder Resolution (CPR) | Conversion factor (m/rot) |
| --- | --- | --- | --- | --- |
| Drive | <br /> | <br /> | <br /> | <br /> |
| Angle | N/A | <br /> | <br /> | <br /> |

### Electrical Configuration

#### Hardware IDs

| Module | Motor CAN IDs | Motor CAN IDs | Encoder CAN IDs | Encoder CAN Bus Channel IDs |
| --- | --- | --- | --- | --- |
| <br /> | Drive | Angle | Absolute Encoder | Absolute Encoder |
| Front Left (FL) | <br /> | <br /> | <br /> |  |
| Front Right (FR) | <br /> | <br /> | <br /> |  |
| Back Left (BL) | <br /> | <br /> | <br /> |  |
| Back Right (BR) | <br /> | <br /> | <br /> |  |

#### 

#### Check Inversion

1. Rotate the *drive* wheel **CCW** (moving “forward”)
   * The built-in encoder value should **increase**. If not, *invert* the drive motor.
2. Rotate the *angle* wheel **CCW** (when viewed from the top)
   * The built-in encoder value should **increase**. If not, *invert* the angle motor.
   * The absolute encoder value should **increase**. If not, *invert* the absolute encoder.
3. Rotate the entire *robot* **CCW**. The gyro angle (yaw) should **increase**. If not, *invert* the IMU

---

| Module | Inverted? | Inverted? | Inverted? | Inverted? |
| --- | --- | --- | --- | --- |
| <br /> | Drive | Angle | Absolute Encoder | IMU |
| Front Left (FL) | <br /> | <br /> | <br /> | <br /> |
| Front Right (FR) | <br /> | <br /> | <br /> | N/A |
| Back Left (BL) | <br /> | <br /> | <br /> | N/A |
| Back Right (BR) | <br /> | <br /> | <br /> | N/A |

### 

### Absolute Encoder Offsets

1. Turn Robot On (Disabled so the wheels can be turned manually).
2. Use module alignment blocks to Turn All 4 wheels so that they are all pointing forward and forward rotation results in increasing drive encoder values (see the black arrows in Orientation Diagram).
3. Measure the absolute encoder value for each module

---

| Module | Absolute Encoder Offset (degrees) | Text |
| --- | --- | --- |
| Front Left (FL) | <br /> | <br /> |
| Front Right (FR) | <br /> | <br /> |
| Back Left (BL) | <br /> | <br /> |
| Back Right (BR) | <br /> | <br /> |



### Input data into the configuration webpage

Open the webpage and import your data into the config files. https://broncbotz3481.github.io/YAGSL-Example/
