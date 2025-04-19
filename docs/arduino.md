# Robotic Dog Arduino Control

This folder contains Arduino code for controlling the servo motors of a four-legged robotic dog using inverse kinematics. Each leg (left front, left back, right front, right back) has three servos to adjust joint angles based on (x, y, z) coordinates input via the Serial Monitor.

## Files

- `Left-Front-Leg-Arduino.ino`: Controls the left front leg's servos.
- `Left-Back-Leg-Arduino.ino`: Controls the left back leg's servos.
- `Right-Front-Leg-Arduino.ino`: Controls the right front leg's servos.
- `Right-Back-Leg-Arduino.ino`: Controls the right back leg's servos.

## Dependencies

- Arduino IDE
- Servo library (included with Arduino)
- `math.h` for trigonometric calculations

## Installation

1. Install Arduino IDE from arduino.cc.
2. Connect three servos per leg to pins 9, 10, and 11 on an Arduino.
3. Upload the appropriate `.ino` file for each leg.

## Usage

1. Open Serial Monitor (9600 baud).
2. Enter x, y, z coordinates when prompted (e.g., "Enter X_centre: ").
3. The code calculates and applies joint angles (T1, T2, T3) to move the servos.
4. Check output for angle values and workspace errors.

## Kinematics

- Segment lengths: a1=4.5 cm, a2=6 cm, a3=5.4 cm.
- Offsets: Left (±1 cm x, ±8.5 cm z), Right (±1 cm x, ±8.5 cm z).
- Angles adjusted with small offsets (T1-5°, T3+6°) for error correction in output values.
