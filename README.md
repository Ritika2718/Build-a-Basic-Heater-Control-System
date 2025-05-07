# Build-a-Basic-Heater-Control-System
# Temperature-Based Heater Control System (ESP32 + Wokwi)

## Problem Statement

Design and implement a simulated embedded system that monitors temperature and controls a heater based on thresholds. The system simulates heating behavior and includes overheating protection and state-based tracking.


## Platform & Tools

- **Simulation**: [Wokwi]([https://wokwi.com/](https://wokwi.com/projects/430305554791987201))
- **Language**: C/C++ (Arduino Framework)
- **Microcontroller**: ESP32 DevKit
- **Sensor**: DHT22 (Temperature Sensor)
- **Optional**: Buzzer (for Overheat alert)

---

## System States

| State            | Description                                          |
|------------------|------------------------------------------------------|
| Idle             | Waiting for valid temperature reading                |
| Heating          | Heater ON - Temperature is below target              |
| Stabilizing      | Heater OFF - Temperature near target                 |
| Target Reached   | Desired temperature achieved                         |
| Overheat         | Temperature exceeds safety limit, alert triggered    |

---

##  Features

- Continuously read temperature from DHT22
- Turn simulated heater ON/OFF based on thresholds
- Log temperature and state over Serial
- Buzzer activates on overheat (optional)
- Easily extendable with FreeRTOS or BLE

---

##  Components Used

| Component | Description |
|----------|-------------|
| ESP32    | Main controller |
| DHT22    | Reads ambient temperature |
| Buzzer   | Optional: Alerts in Overheat state |

---

##  Pin Configuration

| Component | ESP32 GPIO |
|-----------|-------------|
| DHT22     | GPIO4       |
| Buzzer    | GPIO19      |



## Temperature Thresholds

- **Target Temperature**: `30°C`
- **Overheat Temperature**: `40°C`



## Wiring Overview

- **DHT22**: VCC → 3.3V, GND → GND, DATA → GPIO4
- **Buzzer**: + → GPIO19, – → GND


## Simulation Link (Wokwi)

https://wokwi.com/projects/430305554791987201

---

##  Design Document

Refer to the `Design_Document.md` or `Design_Document.pdf` for:
- Sensor selection rationale
- Communication protocol (GPIO - simple, fast, no overhead)
- Block diagram
- Future enhancements roadmap



##  Future Scope

- BLE broadcasting of heater state
- OLED/LCD screen for real-time status
- Multiple heating profiles (e.g., Eco, Turbo)
- Real heater interfacing via MOSFET/Relay
- Smartphone control via app (BLE/WiFi)



## Author

**Ritika Anand**  
B.Tech - Electronics and Communication Engineering  
VIT Chennai



