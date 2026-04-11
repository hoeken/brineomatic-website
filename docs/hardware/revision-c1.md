---
layout: default
title: Revision C1
parent: Hardware
nav_order: 2
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

## Rev C1 Pinout (click to enlarge)

[![Brineomatic Rev C1 Pinout]({{ '/assets/Brineomatic Rev C Pinout.png' | relative_url }})]({{ '/assets/Brineomatic Rev C Pinout.png' | relative_url }})

## Source Files

* [Brineomatic Github Repository](https://github.com/hoeken/brineomatic)
* [Brineomatic Rev C Schematic](https://raw.githubusercontent.com/hoeken/brineomatic/main/schematics/Brineomatic%20Rev%20C1.pdf)
* [3D Printable Case](https://raw.githubusercontent.com/hoeken/brineomatic/refs/heads/main/models/Brineomatic%20Rev%20C%20Case.step)


# Manufacturing

If you would like to manufacture your own boards, follow the instructions below:

## Kicad File Preparation

- Install the Kicad `Fabrication Toolkit` plugin.
- From the PCB Editor, open `Tools -> External Plugins -> Fabrication Toolkit`
- Click `Generate` to create the production files.
- Upload the {board_name}.zip file in the first step of the JLC ordering process
- {board_name}_bom.csv file is the Bill of Materials for PCBA
- {board_name}_positions.csv file is the Component Placement file for PCBA

## JLCPCB Ordering Options

If no option is specified below, use the default options provided by JLCPCB.

### PCB

* PCB Color: Blue
* Surface Finish: ENIG

### Assembly

* Depanel Boards: YES
* PCBA Remark - attach image below
* PCBA Remark - add the text below

```
After production, insert the following parts:
F1 - LCSC C142708
J24 - LCSC C5188250
J7, J12, J14, J16, J25 - LCSC C5188249
J10 - LCSC C71370
```

![SendIt Manufacturing Instructions]({{ 'assets/Brineomatic Rev C1 PCBA Instructions.png' | relative_url }})