---
layout: default
title: Software
nav_order: 3
has_children: true
---

# Software

Brineomatic firmware is fully open source and licensed under the **GPLv3** license.  View the source on [github](https://github.com/hoeken/brineomatic-firmware).

## Firmware Structure

The firmware uses the [YarrboardFramework](https://github.com/hoeken/YarrboardFramework) under the hood:
- Shared channel classes (RelayChannel, ServoChannel, StepperChannel)  
- High-level state machine  
- Real-time FreeRTOS task for automation  
- JSON configuration/validation system
- Multiple API options

## State Machine

Brineomatic transitions through well-defined states:

- **STARTUP** – Initialize hardware, restore state  
- **IDLE** – Waiting, autoflush scheduling  
- **MANUAL** – Direct hardware control  
- **RUNNING** – Production cycle  
- **STOPPING** – Shutdown sequence  
- **FLUSHING** – Freshwater flushing  
- **PICKLING** – Chemical preservation  
- **DEPICKLING** – Re-entry into service  
- **PICKLED** – Long-term storage  

Every stage includes structured safety checks, timeouts, and error recovery.

## Sensor Processing

- Configurable sample averaging  
- 4–20 mA scaling for pressure sensors  
- Temperature-compensated salinity calculation  
- Flowmeter pulse accumulation and volumetric tracking  
- Timed error checks with configurable thresholds  

## Configuration

- JSON config
- General, hardware, and safeguard sections  
- Runtime updates via UI or API