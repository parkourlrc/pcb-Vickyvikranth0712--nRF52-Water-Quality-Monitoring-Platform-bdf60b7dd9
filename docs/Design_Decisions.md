# Design Decisions

## PCB Stack-up

A two-layer PCB was selected to reduce manufacturing cost while maintaining routing flexibility.

---

## Ground Plane

The entire bottom layer is dedicated as a GND copper plane.

Reasons:

- Lower ground impedance
- Better return current path
- Reduced EMI
- Simplified routing

---

## RF Layout

The BLE module antenna keep-out area is preserved.

No copper, traces, or components are placed beneath the antenna.

---

## Power Architecture

Power Flow:

USB Type-C
→ MCP73831 Charger
→ Li-ion Battery
→ MCP1700 LDO
→ 3.3 V Rail
→ nRF52832 Module

---

## Sensor Interface

External JST connectors are used instead of placing sensor modules directly on the PCB.

Reasons:

- Supports multiple sensor vendors
- Easier testing
- Future hardware flexibility

---

## Routing Strategy

- Power traces routed before signal traces.
- Ground plane used for return paths.
- Power trace widths selected using IPC-2152 calculations.
- Manufacturing limits considered during routing.

---

## Net Classes

Separate net classes were created for:

- Power
- Battery
- Digital
- Analog
- SWD

This allows future optimization of routing constraints.

---

## Manufacturing

PCB designed for:

- 2 Layers
- 1 oz Copper
- 1.6 mm Thickness
- Standard PCB fabrication services