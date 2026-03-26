# Circuit Connections

This document explains all the electrical connections used in the project **"Motion Detector Using PIR Sensor"** in a clear and step-by-step manner.

---

## 1. Overview of Connections

The circuit is divided into the following sections:

1. Power Supply Connections  
2. PIR Sensor to 555 Timer  
3. 555 Timer Configuration (Monostable Mode)  
4. RC Timing Network  
5. Transistor Switching Stage  
6. Relay Connections  
7. LED Indicator  

---

## 2. Power Supply Connections

A regulated **5V DC supply** is used for the entire circuit.

| Connection | Description |
|-----------|------------|
| +5V Rail | Connected to VCC of all components |
| GND Rail | Common ground for entire circuit |

### Connect:
- **+5V →**
  - PIR Sensor VCC
  - 555 Timer Pin 8 (VCC)
  - 555 Timer Pin 4 (RESET)
  - One side of relay coil (or relay VCC)
- **GND →**
  - PIR Sensor GND
  - 555 Timer Pin 1 (GND)
  - BC547 Emitter
  - Relay GND

---

## 3. PIR Sensor to 555 Timer

The PIR sensor provides the trigger signal.

| PIR Pin | Connected To |
|--------|-------------|
| VCC | +5V |
| GND | Ground |
| OUT | 555 Timer Pin 2 (Trigger) |

### Note:
- PIR gives **HIGH output on motion detection**
- Depending on configuration, direct connection works in most practical setups

---

## 4. 555 Timer Connections (Monostable Mode)

| Pin No. | Name | Connection |
|--------|------|-----------|
| 1 | GND | Ground |
| 2 | Trigger | From PIR OUT |
| 3 | Output | To transistor base (via resistor) |
| 4 | Reset | +5V (always HIGH) |
| 5 | Control | 10nF capacitor to GND |
| 6 | Threshold | Connected to Pin 7 and capacitor |
| 7 | Discharge | Connected to potentiometer |
| 8 | VCC | +5V |

---

## 5. RC Timing Network

This network controls how long the output stays ON.

### Connections:

- **Potentiometer (100KΩ):**
  - One end → +5V
  - Wiper (middle pin) → Pin 7 (Discharge)

- **Capacitor (470µF):**
  - Positive → Pin 6 (Threshold)
  - Negative → GND

- **Pin 6 and Pin 7 are connected together**

---

## 6. Transistor Switching Stage (BC547)

The transistor is used to drive the relay.

### Connections:

| Transistor Pin | Connected To |
|---------------|-------------|
| Base | 555 Output (Pin 3) via 10K resistor |
| Collector | One side of relay coil |
| Emitter | Ground |

### Working:
- When output of 555 is HIGH → transistor ON  
- When output is LOW → transistor OFF  

---

## 7. Relay Connections

The relay controls the external load.

### Coil Side:

| Relay Pin | Connected To |
|----------|-------------|
| VCC / Coil + | +5V |
| Coil - | Transistor Collector |

### Load Side:

| Terminal | Connection |
|---------|-----------|
| C (Common) | Power source (AC live or DC supply) |
| NO (Normally Open) | Load input |
| Load other end | Neutral / Ground |

### Note:
- Load turns ON when relay is energized

---

## 8. LED Indicator Connection

Used to indicate output status.

### Connection:

- **Anode (+)** → 555 Output (Pin 3)  
- **Cathode (-)** → GND via 1K resistor  

### Function:
- LED ON → Output HIGH → Load ON  
- LED OFF → Output LOW → Load OFF  

---

## 9. Complete Signal Flow

```text
HUMAN MOTION
     ↓
PIR SENSOR (OUT)
     ↓
555 TIMER (Trigger → Output)
     ↓
BC547 TRANSISTOR
     ↓
RELAY
     ↓
LOAD (LIGHT / FAN)
