---
layout: default
title: Rainman Retrofit
parent: Reference Designs
nav_order: 1
---

# SV Phoenix - Rainman Retrofit

The Brineomatic project was started in order to automate my Rainman watermaker on my own personal boat Phoenix.  The goals were to have minimal modifications to the original equipment, and to allow for graceful failure where the watermaker can be switched to manual mode very easily.  All of the critical digital sensors (flowrate, pressure, salinity) have an analog backup, and all of the critical actuated outputs (high pressure valve, diverter valve) can be bypassed to manual mode by removing a few easy to access screws.

## Electrical - High Voltage

My watermaker runs on 230v, so the high voltage electronics are all installed into a waterproof DIN rail enclosure.  This allows for an easy installation, keeps the electronics safe from accidental shorts, as well as keeping everything dry.

For controlling the AC motor, I use a 230v / 63a contactor.  This contactor needs AC voltage for the coil, so I have a small relay that switches the contactor.  The relay is the part that is controlled by Brineomatic.  This has worked great for hundreds of cycles.

Brineomatic itself is powered by a DIN mounted Meanwell 24v PSU.  This provides a clean power supply to Brineomatic, as well as allowing me to have a single breaker to control power to the entire system.

[![Brine-o-Matic 9000 High Voltage Wiring](/assets/Brine-o-Matic 9000-Electrical - High Voltage.drawio.png)](/assets/Brine-o-Matic 9000-Electrical - High Voltage.drawio.pdf)

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