# Troubleshooting Guide

This document lists the most common problems that may occur while building or testing the **Motion Detector Using PIR Sensor** project, along with their possible causes and solutions.

---

## 1. PIR Sensor Output is Always HIGH

### Possible Causes:
- PIR sensor is still in **warm-up / stabilization mode**
- Sensitivity is set too high
- Sensor is detecting continuous movement or heat source
- Wrong wiring connection

### Solutions:
- Wait **30 to 60 seconds** after powering ON the PIR sensor
- Reduce the **sensitivity potentiometer** on the PIR module
- Remove nearby heat sources such as:
  - hot soldering iron
  - sunlight
  - fan heater
  - moving people nearby
- Check wiring:
  - VCC → +5V
  - GND → GND
  - OUT → 555 Trigger Pin

---

## 2. PIR Sensor Does Not Detect Motion

### Possible Causes:
- Wrong PIR wiring
- PIR sensor damaged
- PIR sensitivity too low
- Motion is outside detection range or angle

### Solutions:
- Verify all PIR connections
- Increase PIR sensitivity using onboard potentiometer
- Move hand or body within **3 to 5 meters**
- Test sensor directly with an LED:
  - OUT → LED → resistor → GND
- Replace PIR sensor if no output change occurs

---

## 3. LED is Always ON

### Possible Causes:
- PIR output stuck HIGH
- 555 timer output always HIGH
- Wrong LED connection
- Trigger pin behaving incorrectly

### Solutions:
- First check PIR output separately
- Verify LED is connected correctly:
  - Anode → Output
  - Cathode → Resistor → GND
- Check 555 timer wiring, especially:
  - Pin 2 (Trigger)
  - Pin 3 (Output)
  - Pin 4 (Reset)
  - Pin 6 and Pin 7
- Ensure trigger input is not floating

---

## 4. LED Never Turns ON

### Possible Causes:
- LED polarity reversed
- LED damaged
- 555 timer not triggering
- No power supply

### Solutions:
- Reverse LED terminals if needed
- Test LED directly using 5V and resistor
- Verify output at Pin 3 of 555 timer
- Check power supply voltage
- Make sure PIR output changes when motion is detected

---

## 5. Relay Does Not Click

### Possible Causes:
- Relay not receiving enough current
- Transistor not switching ON
- Wrong transistor pin connection
- Relay coil not connected properly
- No flyback protection or faulty relay

### Solutions:
- Check transistor connections carefully:
  - Base → from 555 output via resistor
  - Collector → relay coil
  - Emitter → GND
- Confirm relay coil gets +5V
- Check whether transistor is saturating properly
- Test relay separately with 5V
- Replace relay if faulty

---

## 6. Relay is Always ON

### Possible Causes:
- 555 output stuck HIGH
- Transistor always ON
- PIR continuously triggering
- Wrong wiring in timer section

### Solutions:
- Check if PIR OUT remains HIGH all the time
- Verify 555 timer trigger logic
- Check transistor base resistor
- Ensure no accidental short between output and +5V
- Inspect RC timing connections

---

## 7. Load Does Not Turn ON Even Though Relay Clicks

### Possible Causes:
- Load connected to wrong relay terminals
- Faulty load
- External supply missing
- NO/NC confusion

### Solutions:
- Connect load through:
  - **C (Common)**
  - **NO (Normally Open)**
- Check if external supply to load is present
- Test load separately
- Do not connect load between wrong terminals

### Correct Relay Load Connection:
```text
Power Source → C
NO → Load
Load Other End → Return Line
