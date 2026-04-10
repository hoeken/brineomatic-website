---
layout: default
title: Rainman Retrofit
parent: Reference Designs
nav_order: 1
---

# Rainman Retrofit

This project was started in order to automate my Rainman watermaker on my own personal boat.  The goals were to have minimal modifications to the original equipment, and to allow for graceful failure where the watermaker can be switched to manual mode very easily.  All of the critical digital sensors (flowrate, pressure, salinity) have an analog backup, and all of the critical actuated outputs (high pressure valve, diverter valve, flush, and boost pump) can be bypassed to manual mode by removing a few easy to access screws.

These files demonstrate how to automate a Rainman watermaker with minimal modification and fail-safe fallback to manual mode.

[![Phoenix Rainman Setup Diagram]({{ '/assets/Phoenix - Rainman Setup.drawio.png' | relative_url }})]({{ '/assets/Phoenix - Rainman Setup.drawio.pdf' | relative_url }})

![Image of Brine-o-matic 9000 Rev A Electronics]({{ '/assets/rainman-install.jpg' | relative_url }})

You can find information on the reference implementation in the files in this repository. They contain example schematics for plumbing, sensors, wiring, AC contactor wiring, etc.

## Files

* [Rainman Plumbing Diagram](https://github.com/hoeken/brineomatic/blob/main/diagrams/Phoenix%20-%20Rainman%20Setup.drawio)
* [Electronics Wiring Diagram](https://github.com/hoeken/brineomatic/blob/main/diagrams/Brine-o-Matic%209000.drawio)
* [3D Printable Control Panel](https://github.com/hoeken/brineomatic/blob/main/models/Rainman%20Control%20Panel%20-%20Rev%20B.step)