# Motion Detector Using PIR Sensor

Automatic Room Lighting and Load Control System using **PIR Sensor, NE555 Timer IC, BC547 Transistor, and Relay**.

This project is a **hardware-based motion detection and automatic load control system** that detects human motion and automatically switches ON a connected load such as a room light or fan. After a preset delay, the load switches OFF automatically when no further motion is detected.

This project was developed as part of the **Applied Electronics Assignment** for **Semester IV**.

---

## 📌 Project Overview

The main purpose of this project is to reduce unnecessary electricity wastage by automating the switching of electrical loads based on human motion detection.

The system works using:
- **PIR Sensor** for motion detection
- **NE555 Timer IC** in monostable mode for delay generation
- **BC547 Transistor** for switching
- **Relay** for controlling the connected load

This project demonstrates the practical application of **sensor interfacing, timer circuits, transistor switching, and relay-based automation**.

---

## 🎯 Objectives

- Detect human motion using a PIR sensor
- Automatically switch ON a connected load
- Keep the load ON for a preset delay period
- Switch OFF the load automatically after timeout
- Demonstrate practical use of:
  - PIR sensor
  - NE555 Timer IC in monostable mode
  - BC547 transistor as a switch
  - Relay-based load control

---

## 🧰 Components Used

| Component | Quantity |
|----------|----------|
| PIR Sensor (HC-SR501) | 1 |
| NE555 Timer IC | 1 |
| BC547 Transistor | 1 |
| 5V Relay | 1 |
| 100K Potentiometer | 1 |
| 470µF Capacitor | 1 |
| 10K Resistor | 1 |
| 1K Resistor | 1 |
| 10nF Capacitor | 1 |
| LED | 1 |
| Breadboard | 1 |
| Jumper Wires | As required |
| 5V Power Supply | 1 |

---

## ⚙️ Working Principle

1. The **PIR sensor** detects human motion and outputs a signal.
2. This signal triggers the **NE555 Timer IC** configured in monostable mode.
3. The 555 timer produces a **HIGH output pulse** for a fixed duration.
4. The output drives the **BC547 transistor**.
5. The transistor energizes the **relay**.
6. The relay switches ON the connected load.
7. After the preset delay, the timer output goes LOW and the load turns OFF automatically.

---

## 🔌 How to Build

1. Connect the **PIR sensor** to the 5V supply and 555 timer trigger input.
2. Configure the **555 timer** in monostable mode.
3. Connect the **output of the 555 timer** to the **BC547 transistor** through a **10K resistor**.
4. Connect the transistor to the **relay coil**.
5. Connect the load through **relay NO and C terminals**.
6. Power the circuit and allow the PIR sensor to stabilize.
7. Move in front of the sensor to test operation.

---

## ⏱️ Timing Formula

The output ON-time of the **555 timer in monostable mode** is given by:

```text
T = 1.1 × R × C
