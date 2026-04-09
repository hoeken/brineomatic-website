---
layout: default
title: Installation & Setup
parent: Software Architecture
nav_order: 1
---

# Installation & Setup

## Building the Firmware
- Install PlatformIO  
- Select the Brineomatic environment  
- Build and upload via USB-C  

## Wiring & Plumbing

See `/diagrams/` for:
- Sensor wiring (flowmeter, tds, pressure, etc)
- Plumbing setup
- Actuator wiring (relays, stepper, and servo)
- Rainman retrofit specifics  

## Network Setup
- Device is configured using Improv Wifi 
- Open `https://www.improv-wifi.com/` in Chrome
- Click either Bluetooth or Serial to configure WiFi.
- Connect to `http://brineomatic.local` or direct to IP
- IP address can be found over serial monitor during bootup

## Initial Configuration
- Declare which sensors are present  
- Declare which actuators are present
- Enter hardware configuration details
- Test each sensor and actuator (MANUAL mode)
- Select desired error checking (more is better)
- Set tank capacity  
- Configure autoflush mode + interval
- Select units (pressure, temperature, flow, etc.)
