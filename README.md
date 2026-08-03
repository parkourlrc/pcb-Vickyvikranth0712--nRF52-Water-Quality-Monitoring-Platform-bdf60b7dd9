# AquaSense – nRF52 Water Quality Monitoring Platform

<p align="center">

![Status](https://img.shields.io/badge/Status-Hardware%20v1.0-success)
![KiCad](https://img.shields.io/badge/KiCad-v10-blue)
![PCB](https://img.shields.io/badge/PCB-2%20Layer-green)
![MCU](https://img.shields.io/badge/MCU-nRF52832-orange)
![License](https://img.shields.io/badge/License-MIT-yellow)

</p>

---

# Overview

AquaSense is a low-power embedded hardware platform designed for modular water quality monitoring applications.

The project is built around the **E73-2G4M04S1B (nRF52832)** Bluetooth Low Energy module and provides a compact battery-powered platform capable of interfacing with multiple external water quality sensors through dedicated JST connectors.

The primary objective of this project was to design a production-style embedded PCB while following industry-standard design practices including:

- Hierarchical schematics
- Modular subsystem design
- IPC-based PCB routing decisions
- Net class management
- RF layout considerations
- Manufacturing-ready outputs

---

# Features

- nRF52832 BLE module (E73-2G4M04S1B)
- USB Type-C power input
- MCP73831 Li-Ion battery charger
- MCP1700 3.3V Low Dropout Regulator
- Battery-powered operation
- SWD programming/debug interface
- Modular JST sensor connectors
- Dedicated ground plane
- RF antenna keep-out region
- Manufacturing-ready Gerbers
- Two-layer PCB

---

# Hardware Architecture

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
              MCP1700 LDO (3.3V)
                     │
        ┌────────────┴────────────┐
        │                         │
        ▼                         ▼
  E73-2G4M04S1B             Status LED
 (nRF52832 BLE Module)
        │
        ├──────────── SWD
        ├──────────── UART
        ├──────────── pH Connector
        ├──────────── TDS Connector
        ├──────────── Turbidity Connector
        └──────────── DS18B20 Connector
```

---

# PCB Specifications

| Parameter | Value |
|------------|-------|
| Layers | 2 |
| PCB Thickness | 1.6 mm |
| Copper Weight | 1 oz |
| Ground Plane | Bottom Layer |
| Manufacturing | Standard 2-layer FR4 |
| Design Software | KiCad 10 |

---

# Components

| Component | Description |
|------------|------------|
| E73-2G4M04S1B | BLE Module (nRF52832) |
| MCP73831 | Li-Ion Battery Charger |
| MCP1700 | 3.3V LDO Regulator |
| USB Type-C | Power Input |
| JST Connectors | External Sensor Interfaces |
| SW Push Button | Reset |
| LED | Status Indicator |

---

# Sensor Interfaces

The PCB is designed to support modular external sensor modules.

Supported interfaces include:

- pH Sensor
- TDS Sensor
- Turbidity Sensor
- DS18B20 Temperature Sensor

Sensor modules are connected through JST headers, allowing flexibility for future sensor upgrades without redesigning the PCB.

---

# Design Decisions

Some of the major engineering decisions made during the design process include:

- Hierarchical schematic architecture
- Bottom-layer GND plane
- Dedicated RF antenna keep-out region
- USB Type-C used only for power input
- MCP73831 configured for approximately 256 mA charging current
- Modular JST sensor connectors
- Power trace widths selected using IPC-2152 calculations with additional engineering margin
- Net classes created for Power, Battery, Analog, Digital and SWD signals

---

# Project Structure

```
nRF52-Water-Quality-Monitoring-Platform/

├── docs/
│   ├── Architecture.md
│   ├── Component_Selection.md
│   ├── Design_Decisions.md
│   ├── Requirements.md
│   └── Revision_History.md
│
├── hardware/
│   ├── Datasheets/
│   ├── KiCad_Project/
│   └── Libraries/
│
├── manufacturing/
│   ├── BOM/
│   ├── Drill/
│   ├── Gerbers/
│   
├── images/
│   ├── PCB/
│   ├── 3D/
│   └── Schematics/
│
├── README.md
└── LICENSE
```

---

# PCB Images

## PCB Layout

> ![PCB Layout](<PCB Layout.png>)

## Ground Plane

> ![Filled Zones](<PCB with Copper Filling.png>)


## 3D Front

> ![Front Side](<Front Side.png>)

---

## 3D Back

> ![Back Side](<Back Side.png>)

# Design Verification

The hardware design has been verified through:

- Electrical Rules Check (ERC)
- Design Rules Check (DRC)
- Manufacturing rule validation
- IPC-guided power trace sizing
- RF keep-out verification
- Gerber generation
- Drill file generation

---

# Manufacturing Outputs

The repository includes:

- Gerber Files
- Excellon Drill Files
- Bill of Materials (CSV)

These outputs are suitable for fabrication using standard PCB manufacturers.

---

# Future Improvements

Future hardware revisions may include:

- Integrated sensor circuitry
- Battery fuel gauge
- Reverse polarity protection
- Lower standby power consumption
- Four-layer PCB revision
- Environmental enclosure integration

---

# Tools Used

- KiCad 10
- Saturn PCB Toolkit
- Git
- GitHub

---

# License

This project is released under the MIT License.

See the LICENSE file for details.

---

# Author

**Vikranth V**

Electronics and Communication Engineering  
SRM Institute of Science and Technology

GitHub: https://github.com/Vickyvikranth0712

LinkedIn: https://www.linkedin.com/in/vikranth1012/

---

⭐ If you found this project interesting, consider starring the repository.
