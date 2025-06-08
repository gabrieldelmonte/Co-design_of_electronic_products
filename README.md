# PBLE01 - Electronic Product Co-design Project

## Overview
This repository contains the complete design files and documentation for PBLE01 - Electronic Product Co-design, a university project developed at UNIFEI (Federal University of Itajubá). The project involves designing a custom printed circuit board (PCB) with microcontroller-based functionality, peripheral interfaces, and power management systems.

## Project Features
- **Microcontroller**: STM32F030K6T6TR (ARM Cortex-M0)
- **Power Supply**: 5V via USB-C with voltage regulation to 3.3V
- **Peripherals**:
  - LCD interface (16x2 character display)
  - 3-button tactile keyboard
  - Status LEDs
  - USB-Serial transceiver (MCP2200)
  - EEPROM memory (24LC512)
  - Light sensor (PDV-P8103 photoresistor)
- **Expansion Interfaces**:
  - SPI connector
  - I²C connector
  - General-purpose GPIO pins
- **Programming Interfaces**: SWD and UART
- **Safety Features**:
  - Overcurrent protection (PPTC fuse)
  - Reverse voltage protection
  - Power indication LEDs

## Technical Specifications
| Parameter             | Value               |
|-----------------------|---------------------|
| PCB Dimensions        | 70 × 70 mm          |
| Layer Count           | 2 (double-sided)    |
| Signal Trace Width    | ≥ 8 mils            |
| Power Trace Width     | ≥ 12 mils           |
| Minimum Spacing       | 8 mils              |
| Minimum Via Diameter  | 12 mils             |
| Operating Voltage     | 5V DC (USB powered) |
| Voltage Regulation    | 3.3V (LD1117S33TR)  |
| Microcontroller Clock | 8 MHz crystal       |

## Repository Structure

```
├── Hardware/
│   └── Projeto_2022014552/ # Complete KiCad design files
├── Documentation/
│   ├── Manual.pdf          # Complete technical documentation
│   ├── Design_Guidelines.pdf
│   └── Requirements.pdf
└── Components/
    └── .../                # Components used in the project Kicad
```

## Design Tools
- **PCB Design**: KiCad v8.99
- **Documentation**: LaTeX/Overleaf
- **Simulation**: Not applicable (hardware-only project)

## Key Design Sections
1. **Power Subcircuit**  
   - USB-C input (USB4215-03-A)
   - Voltage regulation (LD1117S33TR)
   - Power indicators (5V/3.3V LEDs)

2. **Operation Subcircuit**  
   - STM32F030K6 microcontroller
   - 8MHz crystal oscillator
   - Boot mode selection

3. **Peripheral Subcircuit**  
   - USB-Serial interface (MCP2200)
   - EEPROM memory (24LC512)
   - Ambient light sensor (PDV-P8103)

4. **Expansion Interfaces**  
   - SPI (4-wire + power)
   - I²C (2-wire + power)
   - GPIO breakout

## Bill of Materials Highlights
| Component       | Qty | Description            |
|-----------------|-----|------------------------|
| STM32F030K6T6TR | 1   | ARM Cortex-M0 MCU      |
| LD1117S33TR     | 1   | 3.3V Voltage Regulator |
| MCP2200-I/SO    | 1   | USB-UART Bridge        |
| 24LC512-I/SN    | 1   | 512KB EEPROM           |
| PDV-P8103       | 1   | Photoresistor          |
| USB4215-03-A    | 1   | USB-C Connector        |
| JHD162A         | 1   | 16×2 LCD Display       |
| 3296W-1-103RLF  | 1   | 10kΩ Trimmer           |

## Design Validation
- Electrical Rule Check (ERC) passed in KiCad
- Design Rule Check (DRC) compliant with course requirements
- Power consumption analysis included
- Component placement optimized for signal integrity

## Academic Context
Developed for **PBLE01 - Electronic Product Co-design** (2024.2 Semester) at UNIFEI under Prof. Rodrigo de Paula Rodrigues. The project fulfills all course requirements specified in the design guidelines documentation.

## License
This project is for academic purposes. Component datasheets remain property of their respective manufacturers. Design files are provided as-is without warranty.

---

> **Note**: This design has NOT been manufactured yet. See project manual for validation reports and design analysis.
