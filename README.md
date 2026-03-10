# Smart Power Saver for Room

## Overview
This project automatically controls room lighting using a PIR motion sensor and a 555 timer. When motion is detected, the system activates a relay to turn on the light. After a preset delay with no motion, the light turns off automatically.

## Features
- Automatic light control
- Motion detection using PIR sensor
- Adjustable delay using potentiometer
- Low power consumption
- Simple hardware implementation

## Components Used
- PIR Motion Sensor
- NE555 Timer IC
- BC547 Transistor
- 5V Relay Module
- 470µF Capacitor
- 100k Potentiometer
- Resistors
- LED Indicator
- Power Supply (5V)

## Working Principle
1. PIR detects motion.
2. Signal triggers the 555 timer.
3. Timer output activates the relay.
4. Relay switches the load (light).
5. After the delay period, the relay turns off.

## Applications
- Smart homes
- Offices
- Classrooms
- Corridors
- Washrooms

## Future Improvements
- Microcontroller based system
- IoT remote monitoring
- Adjustable motion sensitivity

## Author
Het Patel

