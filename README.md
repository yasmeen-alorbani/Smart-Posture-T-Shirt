# Smart Posture T-Shirt

## Overview

The **Smart Posture T-Shirt** is a wearable posture-monitoring and correction system designed to detect deviations from a user's calibrated posture and provide real-time haptic feedback.

The system integrates an **MPU6050 IMU sensor** with an **ESP32 microcontroller** to continuously monitor changes in body orientation. When the detected posture deviates beyond the defined threshold, vibration motors are activated to alert the user and encourage posture correction.

The project combines wearable hardware, embedded programming, motion sensing, signal filtering, and real-time feedback into a compact and practical prototype.

---

## Objectives

The main objectives of the project are to:

- Monitor the user's posture in real time.
- Detect deviations from a calibrated reference posture.
- Reduce sensor noise through calibration and filtering.
- Provide immediate haptic feedback when poor posture is detected.
- Develop a wearable and practical posture-monitoring prototype.
- Demonstrate the integration of hardware and embedded software in a wearable system.

---

## System Overview

The Smart Posture T-Shirt follows this general workflow:

```text
MPU6050 IMU Sensor
        ↓
   Motion Data
        ↓
   ESP32 Microcontroller
        ↓
Posture Angle Calculation
        ↓
Compare with Reference Angle
        ↓
Posture Deviation Detected?
        ↓
   Vibration Feedback
