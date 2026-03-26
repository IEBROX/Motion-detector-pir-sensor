# Project Summary

## Project Title
**Motion Detector Using PIR Sensor**  
**Automatic Room Lighting and Load Control System**

---

## 1. Introduction

This project is a hardware-based automation system designed to automatically control a light or electrical load based on human motion detection. The system uses a **PIR (Passive Infrared) Sensor** to detect movement and a **NE555 Timer IC** in monostable mode to keep the output active for a preset duration.

When a person enters the sensing area, the system automatically switches ON the connected load. After a fixed time delay, the load turns OFF automatically if no further motion is detected.

This project was developed as part of the **Applied Electronics Assignment** and demonstrates practical implementation of motion-based automation using basic electronic components.

---

## 2. Problem Statement

In homes, hostels, classrooms, offices, and common areas, electrical appliances such as lights and fans are often left ON unnecessarily due to human negligence or forgetfulness. This leads to:

- unnecessary electricity consumption
- increased energy bills
- avoidable power wastage

To solve this problem, an automatic system is needed that can detect human presence and control the load without requiring manual switching.

---

## 3. Objective of the Project

The main objectives of this project are:

- To detect human motion using a PIR sensor
- To automatically switch ON a load when motion is detected
- To keep the load ON for a preset delay period
- To switch OFF the load automatically after the delay
- To understand practical applications of:
  - PIR sensor
  - 555 timer IC
  - transistor switching
  - relay-based load control

---

## 4. Components Used

The following components are used in this project:

- PIR Sensor (HC-SR501)
- NE555 Timer IC
- BC547 NPN Transistor
- 5V Relay
- 100K Potentiometer
- 470µF Capacitor
- 10K Resistor
- 1K Resistor
- 10nF Capacitor
- LED
- Breadboard
- Jumper Wires
- 5V DC Power Supply

---

## 5. Working Principle

The working of the project is based on motion detection and timed switching.

### Step-by-step working:
1. The **PIR sensor** continuously monitors the surrounding area.
2. When human motion is detected, the PIR sensor gives an output signal.
3. This signal triggers the **555 Timer IC**.
4. The 555 timer produces a HIGH output for a fixed duration.
5. This output drives the **BC547 transistor**.
6. The transistor activates the **relay**.
7. The relay switches ON the connected load.
8. After the preset time delay, the timer output becomes LOW.
9. The relay turns OFF and the load is disconnected.

This process allows the load to operate automatically without manual intervention.

---

## 6. Timing Calculation

The 555 timer is used in **Monostable Mode**, and its ON-time is given by:

```text
T = 1.1 × R × C
