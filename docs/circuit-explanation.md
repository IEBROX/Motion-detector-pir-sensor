# Circuit Explanation

## Overview
The Smart Power Saver for Room is an automatic lighting control system that uses a PIR motion sensor and a 555 timer to switch room lights ON when motion is detected and OFF after a preset delay. The system reduces unnecessary energy consumption by ensuring lights are only active when someone is present.

---

## Main Components

| Component | Function |
|----------|-----------|
| PIR Sensor | Detects human motion using infrared radiation |
| NE555 Timer IC | Generates a time delay for the light to remain ON |
| BC547 Transistor | Acts as a switch to control the relay |
| Relay Module | Switches the electrical load (light) |
| Capacitor (470 µF) | Determines the delay time |
| Potentiometer (100k) | Adjusts the delay duration |
| Resistors | Control current flow in the circuit |
| LED Indicator | Shows timer output status |
| Power Supply (5V) | Provides power to the system |

---

## Working Principle

1. The PIR sensor detects motion by sensing changes in infrared radiation caused by a human body.
2. When motion is detected, the PIR sensor outputs a HIGH signal.
3. This signal triggers the NE555 timer configured in monostable mode.
4. The timer output (pin 3) becomes HIGH for a fixed period determined by the RC timing network.
5. The BC547 transistor amplifies the signal and activates the relay module.
6. The relay connects the power supply to the light.
7. The light remains ON for the preset delay time.
8. After the delay expires and no motion is detected, the relay turns OFF and the light switches OFF.

---

## Timing Calculation

The delay time of the NE555 timer is calculated using the formula:

T = 1.1 × R × C

Where:
- **T** = Time delay  
- **R** = Resistance (Potentiometer value)  
- **C** = Capacitance (Timing capacitor)

Example:

- R = 100kΩ  
- C = 470µF  

T ≈ 1.1 × 100000 × 0.00047
T ≈ 51 seconds

This means the light stays ON for approximately **50 seconds after motion detection**.

---

## Signal Flow

Motion Detected
↓
PIR Sensor Output
↓
555 Timer Trigger
↓
Timer Output HIGH
↓
BC547 Transistor ON
↓
Relay Activated
↓
Light Turns ON

After the delay:

Timer Output LOW
↓
Relay OFF
↓
Light OFF


---

## Advantages

- Reduces electricity wastage
- Automatic operation
- Low cost and easy to implement
- Adjustable delay time
- Reliable motion detection

---

## Applications

- Smart homes
- Offices
- Classrooms
- Corridors
- Washrooms
- Storage rooms

---

## Possible Improvements

- Integration with microcontrollers (Arduino / ESP32)
- IoT-based remote monitoring
- Adjustable motion sensitivity
- Multiple sensor integration for large rooms

---

## Conclusion

This project demonstrates an effective method for reducing power consumption by automatically controlling room lighting based on motion detection. The combination of a PIR sensor and NE555 timer provides a simple, low-cost, and reliable solution for smart lighting systems.
