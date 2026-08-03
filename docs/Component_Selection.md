# Component Selection

## E73-2G4M04S1B (nRF52832 BLE Module)

Selected because:

- Integrated Bluetooth Low Energy radio
- Compact RF-certified module
- Low power consumption
- Built-in antenna
- Simplifies RF PCB design

Alternatives Considered:

- ESP32-C3
- Bare nRF52832 SoC

---

## MCP73831 Li-Ion Charger

Selected because:

- Single-cell Li-ion charging IC
- Programmable charging current
- Minimal external components
- Suitable for USB-powered charging

Charging Current:

- Programming resistor: 3.9 kΩ
- Charge current ≈ 256 mA

---

## MCP1700 LDO Regulator

Selected because:

- Low quiescent current
- Low dropout voltage
- Stable 3.3 V output
- Suitable for battery-powered systems

---

## USB Type-C Connector

Purpose:

- 5 V power input only
- USB data lines not used
- CC pins configured with 5.1 kΩ pull-down resistors

---

## JST Connectors

Selected for modular sensor interfacing.

Connectors:

- pH Sensor
- TDS Sensor
- Turbidity Sensor
- DS18B20 Temperature Sensor

Advantages:

- Easy replacement
- Modular testing
- Future sensor upgrades

---

## Passive Components

0603 SMD package selected for:

- Easy hand soldering
- Wide availability
- Compact PCB layout