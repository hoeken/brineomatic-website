---
layout: default
title: Sensors and Actuators
parent: Hardware
nav_order: 3
---

# Sensors

## Pressure Sensors

Brineomatic supports standard 4–20 mA analog pressure sensors for monitoring filter inlet and membrane pressure.  These sensors are powered by the same voltage that powers the board (12v/24v).

Typically you will want a 0-1000psi sensor for the high pressure side, and a 0-50psi sensor for the low pressure side.

### Verified Suppliers

* [DataQ](https://www.dataq.com/products/accessories/pressure-sensor/)

### TDS / Salinity Sensors

TDS (Total Dissolved Solids) sensor inputs are provided for measuring product water and brine salinity.  The inputs are designed to interface with the DFRobot TDS Sensor boards.

### Verified Suppliers

* [DFRobot](https://wiki.dfrobot.com/sen0244)

### Flow Meters (Pulse)

Pulse-type flow meter inputs are supported for measuring product and brine flow rates.  These flowmeters should accept 5v power and have an open collector output.  This is the most common type.

### Verified Suppliers

* [Amazon Flowmeter](https://www.amazon.com/dp/B07MY7H45V) - Push fit connector style is simple to use, cheap, and reliable
* [Omega BV2000TRN075B](https://www.dwyeromega.com/) - These parts are hard to get an expensive.

### Temperature Sensors (DS18B20)

DS18B20 digital temperature sensor inputs are available for monitoring motor and water temperature.

### Verified Suppliers

* Any DS18B20 sensor will work.  Readily available on Amazon, etc.

# Actuators

## Relays / Solenoid Drivers

Brineomatic provides relay/solenoid driver outputs (3A max each) for controlling solenoid valves and other loads.  Loads will be powered with the same voltage supplying the board (12v/24v)

You can power low-power things like relays, contactors, fans, and solenoid valves directly.  Larger loads like big AC or DC motors will require using a relay or contactor wired to the Brineomatic relay channel.

## Stepper Motor

An onboard stepper motor driver is available for controlling the high pressure valve.  The ideal stepper motor is a 0.5A to 1.5A, NEMA17 motor.  These are readily available on Amazon, etc.

## DC Servos

5V servo connectors are provided for standard RC-style servo actuators to open and control valves.  Brineomatic has a maximum 3A output, so using a servo motor that is too large may cause the board to brown-out and reset.  Most hobbyist size servos will be compatible.

### Verified Suppliers

[Hitec HS-422](https://www.hiteccs.com/actuators/product-details/HS-422)

## VFD / RS485

RS485 Modbus support allows control of Variable Frequency Drive (VFD) pump controllers such as the [INVT GD20](https://www.invt.com/products/gd20-series-vfd-14)