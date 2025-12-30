# OpenMustang Architecture

## Overview
OpenMustang follows a **modular, distributed architecture**

Each cockpit subsystem is designed as an **independent module** with its own:
- mechanical structure
- electronics
- firmware
- documentation

This approach allows parallel development, easier debugging, and long-term
scalability.

---

## Core Principles

### Modular Design
- Each module is self-contained
- Modules can be developed, tested, and replaced independently
- No single point of failure for the entire cockpit

### USB HID-Based Interface
- Every active module appears to the PC as a **USB HID device**
- DCS World detects modules as joysticks, throttles, or button panels
- No custom drivers required

### DIY-Friendly Manufacturing
- 3D printing as primary manufacturing method
- Optional CNC / laser-cut parts
- Simple, reproducible PCB designs

---


Each module:
- Uses its own microcontroller (arduino)
- Handles its own sensors, switches, and outputs
- Communicates directly with the PC

---

## Electronics Philosophy

- No central master controller in early phases
- Distributed USB HID devices for simplicity
- Future consolidation is optional, not required

---

## Firmware Guidelines

- Simple, readable code
- HID-compliant
- No closed-source dependencies
- Module-specific firmware lives inside each module folder

---

## Mechanical Philosophy

- Accuracy over extreme realism where it benefits DIY builders
- Tolerances designed for FDM printing
- Serviceability prioritized over visual perfection

---

## Licensing Considerations

- CAD, documentation, and design files: **CC BY-NC-SA 4.0**
- Firmware may use a different license if required (clearly stated per module)
- Commercial use is not permitted without explicit permission

---

## Long-Term Vision
OpenMustang aims to become a **reference DIY P-51D cockpit project** that:
- Is approachable for beginners
- Scales to advanced builds
- Encourages learning and collaboration

