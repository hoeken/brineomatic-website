---
layout: default
title: Overview
nav_order: 1
---

# Brineomatic — Open Hardware Watermaker Automation Controller

Brineomatic is an open-hardware, open-firmware watermaker controller that fully automates a marine reverse-osmosis watermaker. Designed for DIY, builders, and cruising sailors, it provides **full cycle automation**, **robust safety checks**, and **modern web-based control**.  All of this while remaining easy to service, modify, and adapt to nearly any watermaker—including Rainman, DIY builds, and traditional AC pump systems.

Built on the **ESP32-S3**, Brineomatic integrates pressure sensors, flow meters, temperature sensing, and salinity monitoring with intelligent control of pumps, valves, and a high-pressure valve stepper motor. It automates the entire operating lifecycle: production runs, freshwater flushes, safety shutdowns, and chemical pickling/depickling.

### User Interface
![Brineomatic Running - Typical interface during a run cycle.]({{ '/assets/brineomatic-running.png' | relative_url }})

### Hardware 
![Brineomatic Running - Typical interface during a run cycle.]({{ 'assets/Brineomatic Rev C Case.jpg' | relative_url }})

---

# Features

## Automation
- Automatic run cycles  
- Time-based, volume-based, or salinity-based production  
- Automatic freshwater flush (time / volume / salinity modes)  
- Full pickling + depickling sequences  
- Manual mode for direct hardware testing and setup
- Tank-level-based stop support  
- NTP-synced autoflush intervals  

## Safety
Brineomatic continuously monitors critical values and stops safely on failure:
- High/low membrane pressure  
- High/low filter pressure  
- High product salinity  
- Low product/brine flowrate  
- Low total flowrate (combined)  
- Diverter valve closed failure  
- Motor over-temperature  
- Flush valve stuck open  
- Low Battery
- Low Tank Level (flushing)
- Comprehensive timeout handling

## User Interface
- Local HTML5 web interface served directly from the ESP32  
- Fast, mobile-friendly design  
- Works on phones, laptops, and supported MFDs  
- Real-time dashboard with flow, pressure, salinity, temperature, and tank level  
- Full configuration editor - no editing config files  
- Optional sound notifications (success/error melodies)  

## Integrations
- MQTT publishing
- SignalK 
- Home Assistant
- HTTP/REST endpoints  
- WebSocket real-time control