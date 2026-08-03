# Hardware Architecture

## System Overview

```
                USB Type-C
                     │
                     ▼
              MCP73831 Charger
                     │
                     ▼
             Li-Ion Battery Cell
                     │
                     ▼
              MCP1700 LDO (3.3 V)
                     │
        ┌────────────┴────────────┐
        │                         │
        ▼                         ▼
  E73-2G4M04S1B             Status LED
 (nRF52832 BLE Module)
        │
        ├──────────── SWD Header
        │
        ├──────────── UART Header
        │
        ├──────────── pH Connector
        │
        ├──────────── TDS Connector
        │
        ├──────────── Turbidity Connector
        │
        └──────────── DS18B20 Connector
```

---

## Subsystems

### USB Power Input

Provides 5 V input through USB Type-C.

---

### Battery Charging

Handled by MCP73831 using a constant-current / constant-voltage charging algorithm.

---

### Voltage Regulation

Battery voltage is regulated to 3.3 V using the MCP1700 LDO.

---

### BLE Processing

The E73-2G4M04S1B module performs:

- Sensor data acquisition
- BLE communication
- Control logic

---

### Sensor Expansion

External JST connectors allow modular connection of sensors.