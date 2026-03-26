# Smart Power Saver for Room

A smart energy-saving room automation project developed for **Applied Electronics (AE)**.  
This system is designed to automatically control room appliances such as lights and fans based on room occupancy and environmental conditions, helping reduce unnecessary electricity consumption.

---

## 📌 Project Overview

In many rooms, lights and fans are often left ON even when no one is present, leading to unnecessary power wastage.  
The **Smart Power Saver for Room** solves this problem by using sensors and a control unit to detect room conditions and automatically operate electrical loads only when required.

This project demonstrates a practical application of **automation**, **sensing**, and **power control** in a simple and cost-effective way.

---

## 🎯 Objective

The main objective of this project is to:

- Reduce unnecessary power consumption in a room
- Automate the operation of room appliances
- Improve energy efficiency using sensors and electronics
- Build a low-cost smart room control system

---

## 🚀 Features

- Automatic room light control
- Occupancy/person detection
- Smart power saving operation
- Low-cost and beginner-friendly design
- Suitable for homes, classrooms, offices, and hostels
- Can be expanded for IoT-based automation in future

---

## 🛠 Components Used

| Component | Quantity | Description |
|----------|----------|-------------|
| Microcontroller / Control Unit | 1 | Used to process sensor inputs and control outputs |
| PIR Sensor / IR Sensor | 1 | Detects human presence or motion |
| LDR Sensor *(if used)* | 1 | Detects ambient light intensity |
| Relay Module | 1 | Controls electrical load |
| LED / Bulb | 1 | Represents room light |
| Fan / DC Motor *(optional)* | 1 | Represents room fan |
| Breadboard / PCB | 1 | Circuit assembly |
| Connecting Wires | Multiple | Electrical connections |
| Power Supply | 1 | Provides operating voltage |

---

## ⚙ Working Principle

The working of the system is based on automatic sensing and control:

1. The sensor continuously monitors the room for human presence or motion.
2. When a person enters the room, the sensor sends a signal to the control unit.
3. The control unit processes the signal and turns **ON** the connected appliance (light/fan).
4. When no person is detected for a certain time, the system turns the appliance **OFF** automatically.
5. If an **LDR sensor** is used, the system can also decide whether the light should turn ON only when the room is dark.

This helps in minimizing electricity wastage and improving energy efficiency.

---

## 🧠 System Logic

### Basic Logic

- **Person detected** → Appliance ON
- **No person detected** → Appliance OFF after delay
- **Dark room (if LDR used)** → Light ON
- **Bright room (if LDR used)** → Light OFF

---

