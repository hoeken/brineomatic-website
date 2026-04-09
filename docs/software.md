---
layout: default
title: Software Architecture
nav_order: 3
---

# Software Architecture

## Firmware Structure

The firmware uses the Yarrboard modular ecosystem:
- Shared channel classes (RelayChannel, ServoChannel, StepperChannel)  
- High-level state machine  
- Real-time FreeRTOS task for automation  
- Non-blocking I/O  
- ADS1115 averaging helpers  
- OneWire/DS18B20 sensor handling  
- JSON configuration/validation system  

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

- JSON config for each backup  
- General, hardware, and safeguard sections  
- Runtime updates via UI or API  
- EEPROM last flush time persistence  
