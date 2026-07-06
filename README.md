# STM32 Telemetry Board

> An end-to-end embedded systems project covering hardware design, firmware development, and desktop software for an STM32-based telemetry board.

![Project Status](https://img.shields.io/badge/Status-In%20Development-orange)
![MCU](https://img.shields.io/badge/MCU-STM32-blue)
![PCB](https://img.shields.io/badge/PCB-KiCad-success)
![Language](https://img.shields.io/badge/Firmware-C-informational)
![Desktop](https://img.shields.io/badge/Desktop-Python-yellow)

---

# Overview

This project documents the complete development of an embedded telemetry board built around an STM32 microcontroller.

The objective is to design every part of the system from scratch while following industry-standard embedded development practices.

The project includes:

- Custom PCB design using KiCad
- STM32 firmware development in C
- Temperature acquisition through an I²C sensor
- UART communication with a desktop application
- Python desktop interface
- Complete engineering documentation
- Version control using Git

---

# System Architecture

```
                  USB-C
                    │
                    ▼
             +--------------+
             | 3.3V Regulator|
             +------+-------+
                    │
                    ▼
           +------------------+
           |  STM32C091KB MCU |
           +--------+---------+
                    │
         ┌──────────┴──────────┐
         │                     │
         ▼                     ▼
    TMP102 Sensor         UART Interface
      (I²C)                     │
                                ▼
                     Python Desktop Software
```

A more detailed architecture description is available in:

```
docs/System_Architecture.md
```

---

# Features

### Hardware

- STM32 microcontroller
- TMP102 digital temperature sensor
- USB powered
- 3.3V regulated supply
- UART communication
- I²C sensor interface
- Status LED

### Firmware

- Bare-metal C
- GPIO drivers
- I²C communication
- UART communication
- Periodic telemetry transmission

### Desktop Software

- Python application
- Real-time temperature display
- Telemetry monitoring
- Data logging *(planned)*

---

# Project Status

## Hardware

- [x] System specifications
- [x] Component selection
- [x] Schematic design
- [x] PCB layout
- [x] ERC verification
- [x] DRC verification
- [ ] PCB manufacturing
- [ ] Hardware validation

## Firmware

- [ ] STM32CubeMX configuration
- [ ] Clock configuration
- [ ] GPIO driver
- [ ] I²C driver
- [ ] UART driver
- [ ] Temperature acquisition
- [ ] Telemetry protocol

## Desktop Application

- [ ] User interface
- [ ] Live telemetry
- [ ] Data logging
- [ ] Graph visualization

---

# Repository Structure

```
docs/
│
├── Specifications.md
├── System_Architecture.md
├── Component_Selection.md
├── PCB_Design.md
└── Test_Plan.md

hardware/
│
├── kicad/
├── datasheets/
└── gerbers/

firmware/

software/

images/
```

---

# Technologies

- STM32
- KiCad
- C
- Python
- PySide6
- Git
- UART
- I²C
- USB

---

# Roadmap

## Version 1.0

- Complete PCB design
- Manufacture PCB
- Assemble components
- Develop firmware
- Read temperature sensor
- Display data on desktop application

## Future Improvements

- Additional sensors
- CAN communication
- RS-485 interface
- BLE connectivity
- Bootloader support
- FreeRTOS integration

---

# Documentation

Detailed design documents are available inside the `docs/` directory.

These documents include:

- System specifications
- Architecture
- Component selection
- PCB design choices
- Test plan

---

# License

This project is licensed under the MIT License.

---

# Author

**Mor Talla Niang**

Embedded Systems Engineer

France
