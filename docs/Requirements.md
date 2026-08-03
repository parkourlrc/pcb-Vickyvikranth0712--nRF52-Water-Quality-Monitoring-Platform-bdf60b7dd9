# AquaSense Hardware Requirements

## Project Overview

AquaSense is a battery-powered nRF52832-based embedded platform designed for water quality monitoring. The hardware focuses on providing a modular, low-power architecture capable of interfacing with multiple external water quality sensors.

---

## Functional Requirements

- Interface with external water quality sensors through dedicated JST connectors.
- Support pH, TDS, Turbidity, and DS18B20 temperature sensors.
- Provide Bluetooth Low Energy (BLE) communication through the E73-2G4M04S1B (nRF52832) module.
- Support firmware programming and debugging through an SWD interface.
- Provide battery charging through USB Type-C using the MCP73831 Li-ion charging IC.
- Regulate battery voltage to 3.3 V using the MCP1700 low-dropout regulator.
- Include visual charging status indication using an LED.
- Support future expansion through external connectors.

---

## Electrical Requirements

- Input Supply: USB Type-C (5 V)
- Battery: Single-cell Li-ion (3.7 V nominal)
- System Voltage: 3.3 V
- PCB Layers: 2
- Copper Thickness: 1 oz
- PCB Thickness: 1.6 mm

---

## Design Constraints

- Two-layer PCB construction.
- Bottom-layer ground plane.
- RF keep-out area maintained beneath the BLE antenna.
- Manufacturing rules compatible with standard PCB fabrication services.
- Trace widths selected based on IPC-2152 calculations with additional design margin.

---

## Future Enhancements

- Integrated sensor circuits instead of connector-based modules.
- Ultra-low-power optimization.
- Battery fuel gauge integration.
- Reverse polarity protection.
- Environmental enclosure integration.