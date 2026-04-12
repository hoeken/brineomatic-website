---
layout: default
title: Rainman Retrofit
parent: Reference Designs
nav_order: 1
---

# Rainman Retrofit

The Brineomatic project was started in order to automate my Rainman watermaker on my own personal boat Phoenix.  The goals were to have minimal modifications to the original equipment, and to allow for graceful failure where the watermaker can be switched to manual mode very easily.  All of the critical digital sensors (flowrate, pressure, salinity) have an analog backup, and all of the critical actuated outputs (high pressure valve, diverter valve) can be bypassed to manual mode by removing a few easy to access screws.

## Control Panel

![Image of Brine-o-matic 9000 Rev A Electronics](/assets/rainman-install.jpg)

### Diverter Valve

![Diverter Valve Diagram](/assets/phoenix diverter valve diagram.png)

### High Pressure Valve

![High Pressure Valve Diagram](/assets/phoenix high pressure valve stepper diagram.png)

![High Pressure Valve Cutaway](/assets/phoenix high pressure valve cutaway.png)


## Plumbing Block Diagram

[![Phoenix Rainman Setup Diagram](/assets/Phoenix - Rainman Setup.drawio.png)](/assets/Phoenix - Rainman Setup.drawio.pdf)

## Files

* [Rainman Plumbing Diagram - Drawio](https://github.com/hoeken/brineomatic/blob/main/diagrams/Phoenix%20-%20Rainman%20Setup.drawio)
* [Electronics Wiring Diagram - Drawio](https://github.com/hoeken/brineomatic/blob/main/diagrams/Brine-o-Matic%209000.drawio)
* [3D Printable Control Panel - STEP file](https://github.com/hoeken/brineomatic/blob/main/models/Rainman%20Control%20Panel%20-%20Rev%20B.step)