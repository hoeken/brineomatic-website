---
layout: default
title: Reference Designs
nav_order: 7
---

# Reference Designs

## Rainman Retrofit

This project was started in order to automate my Rainman watermaker on my own personal boat.  The goals were to have minimal modifications to the original equipment, and to allow for graceful failure where the watermaker can be switched to manual mode very easily.  All of the critical digital sensors (flowrate, pressure, salinity) have an analog backup, and all of the critical actuated outputs (high pressure valve, diverter valve, flush, and boost pump) can be bypassed to manual mode by removing a few easy to access screws.

These files demonstrate how to automate a Rainman watermaker with minimal modification and fail-safe fallback to manual mode.

![Image of Brine-o-matic 9000 Rev A Electronics](/assets/rainman-install.jpg)

You can find information on the reference implementation in the files in this repository. They contain example schematics for plumbing, sensors, wiring, AC contactor wiring, etc.

There is also a 3D model with a control panel layout and parts for automating a Rainman watermaker.  This is available as a STEP file that should be editable with FreeCAD.  The actual design was done in Fusion360 which is available through the link below.

## Adapting to Other Watermakers
Guidance for:
- AC high-pressure pumps  
- DC gear pumps  
- Commercial RO units  
- DIY builds  
