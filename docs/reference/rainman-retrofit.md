---
layout: default
title: Rainman Retrofit
parent: Reference Designs
nav_order: 1
---

# Rainman Retrofit

This project was started in order to automate my Rainman watermaker on my own personal boat.  The goals were to have minimal modifications to the original equipment, and to allow for graceful failure where the watermaker can be switched to manual mode very easily.  All of the critical digital sensors (flowrate, pressure, salinity) have an analog backup, and all of the critical actuated outputs (high pressure valve, diverter valve) can be bypassed to manual mode by removing a few easy to access screws.

![Image of Brine-o-matic 9000 Rev A Electronics]({{ '/assets/rainman-install.jpg' | relative_url }})

Here is the block diagram of my retrofit with part numbers:

[![Phoenix Rainman Setup Diagram]({{ '/assets/Phoenix - Rainman Setup.drawio.png' | relative_url }})]({{ '/assets/Phoenix - Rainman Setup.drawio.pdf' | relative_url }})

Here are the source files for everything, including the 3d printed parts.

## Files

* [Rainman Plumbing Diagram - Drawio](https://github.com/hoeken/brineomatic/blob/main/diagrams/Phoenix%20-%20Rainman%20Setup.drawio)
* [Electronics Wiring Diagram - Drawio](https://github.com/hoeken/brineomatic/blob/main/diagrams/Brine-o-Matic%209000.drawio)
* [3D Printable Control Panel - STEP file](https://github.com/hoeken/brineomatic/blob/main/models/Rainman%20Control%20Panel%20-%20Rev%20B.step)