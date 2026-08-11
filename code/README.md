
# Smart Posture T-Shirt – Control Code

## Overview

This folder contains the Arduino code for the Smart Posture T-Shirt prototype.

The system uses an **MPU6050 accelerometer/gyroscope sensor** to monitor the user's posture by measuring changes in the body angle. The measured posture is compared with a calibrated reference angle. When the deviation exceeds the defined posture threshold, three vibration motors are activated to provide real-time feedback.

## Main Components

- MPU6050 motion sensor
- Three vibration motors
- Microcontroller
- I2C communication

## How the System Works

1. The system initializes the MPU6050 sensor.
2. The sensor connection is checked.
3. The system allows the sensor to stabilize.
4. The MPU6050 is calibrated using 3000 samples.
5. A reference posture angle is recorded.
6. The current posture angle is continuously calculated.
7. The current angle is compared with the reference angle.
8. If the posture deviation exceeds **2 degrees**, all three motors are activated.
9. When the posture returns within the acceptable range, the motors are deactivated.

## Posture Detection

The posture angle is calculated using the accelerometer readings from the X and Z axes.

The accelerometer readings are converted to `g` units and processed using a low-pass filter to reduce sudden fluctuations.

The posture angle is calculated using:

```cpp
atan2(filteredAx, filteredAz)
