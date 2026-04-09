---
layout: default
title: Revision C1
parent: Hardware
nav_order: 1
---

# Revision C1

Revision C1 is the latest version of the Brineomatic board.

## Core capabilities:

- ESP32-S3 module with WiFi and USB-C  
- 12–30 V DC input with onboard power regulation  
- 5 × relay/solenoid drivers (3A max)
- 1 × stepper motor driver
- 2 × 5V servo connectors  
- 2 × flowmeter inputs (product + brine)  
- 2 × TDS connectors (product + brine)
- 2 × 4–20 mA pressure sensor inputs (filter + membrane)  
- 2 x DS18B20 motor temperature sensor  
- Optional RS485 Modbus VFD pump support (GD20, etc.)  
- I²C expansion (QWIIC)

## Sensors and Inputs

- Filter pressure (4–20 mA)  
- Membrane pressure (4–20 mA)  
- Product salinity (TDS)  
- Brine salinity (TDS)  
- Product flowrate (pulse)  
- Brine flowrate (pulse)  
- Motor temperature (DS18B20)  
- Water temperature (DS18B20)  

## Rev C1 Pinout

![Brineomatic Rev C1 Pinout]({{ '/assets/Brineomatic Rev C Pinout.png' | relative_url }})

## Source Files

* [Brineomatic Github Repository](https://github.com/hoeken/brineomatic)
* [Brineomatic Rev C Schematic](https://raw.githubusercontent.com/hoeken/brineomatic/main/schematics/Brineomatic%20Rev%20C1.pdf)
* [3D Printable Case](https://raw.githubusercontent.com/hoeken/brineomatic/refs/heads/main/models/Brineomatic%20Rev%20C%20Case.step)
