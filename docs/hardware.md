---
layout: default
title: Hardware
nav_order: 2
---

# Hardware

## Controller Board

Brineomatic is built around the ESP32-S3 with USB-C, using modular Yarrboard channels for relays, servos, steppers, and IO expansion.

### Rev C Pinout

![Brineomatic Rev C Pinout]({{ '/assets/Brineomatic Rev C Pinout.png' | relative_url }})

### Rev B Pinout

![Brineomatic Rev B Pinout]({{ '/assets/Brineomatic Rev B Pinout.png' | relative_url }})

### Core capabilities:
- ESP32-S3 module with WiFi and USB-C  
- 12–30 V DC input with onboard power regulation  
- 4 × relay/solenoid drivers  
- 1 × stepper motor driver  
- 2 × 5V servo connectors  
- 2 × flowmeter inputs (product + brine)  
- 2 × TDS connectors (product + brine)
- 2 × 4–20 mA pressure sensor inputs (filter + membrane)  
- DS18B20 motor temperature sensor  
- Optional Modbus VFD pump support (GD20, etc.)  
- Cooling fan output  
- I²C expansion + test points (3.3V, 5V, 24V, SDA, SCL, GND)

## Sensors and Inputs

- Filter pressure (4–20 mA)  
- Membrane pressure (4–20 mA)  
- Product salinity (TDS)  
- Brine salinity (TDS)  
- Product flowrate (pulse)  
- Brine flowrate (pulse)  
- Motor temperature (DS18B20)  
- Water temperature (for salinity compensation)  
- Tank level (via SignalK or API)

## Outputs

- Boost pump (relay)  
- High-pressure pump (relay or Modbus VFD)  
- High-pressure valve (stepper motor)  
- Diverter valve (servo)  
- Flush valve (relay)  
- Cooling fan (relay)

## Mechanical Files

- Controller case (STEP)  
- Rainman retrofit control panel (STEP)  
- Fusion 360 reference assembly
