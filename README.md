# Industrial IoT Gateway with OPC UA and TSN Emulation

This project demonstrates an Industrial IoT Gateway built on a Raspberry Pi, showcasing OPC UA for standardized data exchange and emulating Time-Sensitive Networking (TSN) for deterministic communication.
![Gateway](https://github.com/sidortal/OBB-Expansion/blob/main/IoT-Gateway-Features-768x432.png)
---

## Project Overview

The goal is to create a gateway that bridges industrial devices and cloud systems, using industry-standard protocols. The Raspberry Pi acts as a central hub, collecting data from simulated or real industrial sensors, exposing it via OPC UA, and emulating TSN for real-time data transmission.

![Industry 4.0](https://github.com/sidortal/OBB-Expansion/blob/main/indus4.0.png)
---

## Hardware

- **Raspberry Pi 4 (or Compute Module 4):** The core processing unit.
- **Ethernet Cable (Cat5e/Cat6):** For network connectivity and TSN emulation.
- **Power Supply (5V, 3A):** To power the Raspberry Pi.
- **Optional:**
  - CAN Bus Transceiver (MCP2551) and CAN Bus Cable (for CAN devices).
  - Serial to USB adapter (for serial devices).
  - Industrial Sensors/Actuators (for testing).

---

## Hardware Diagram

![Industrial IoT Gateway Diagram](https://github.com/sidortal/OBB-Expansion/blob/main/IOTgateway.jpg)


---

## Software Stack

- **OPC UA Server:** Built using open62541 or node-opcua (depending on language preference).
- **TSN Emulation Layer:** Simulated using time-synchronized data scheduling and Linux PREEMPT-RT patch.
- **MQTT Client:** For sending selected data to the cloud.
- **Cloud Backend:** AWS IoT Core, Azure IoT Hub, or a custom server for storing and visualizing data.

---

## Setup Instructions

![Industry 4.0](https://github.com/sidortal/OBB-Expansion/blob/main/warehouse.jpg)

### 1. OS and Dependencies

- Flash Raspberry Pi OS (Lite or Full) to SD card.
- Install required packages:

```bash
sudo apt update
sudo apt install cmake git build-essential libpaho-mqtt-dev
