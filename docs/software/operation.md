---
layout: default
title: Operation
parent: Software
nav_order: 3
---

# Operation

## Normal Run Cycle
Supports three modes:
- **Tank Fill**  
- **Time-based**  
- **Volume-based**  

Brineomatic will:
1. Initialize hardware  
2. Pre-pressurize via boost pump  
3. Ramp high-pressure pump  
4. Wait for membrane pressure  
5. Verify product flowrate  
6. Verify product salinity  
7. Close diverter valve  
8. Produce water while watching for errors  
9. Stop based on time, volume, tank level, or user  
10. Finish with autoflush

## Flush Cycle
Supports three modes:
- **Time-based**  
- **Volume-based**  
- **Brine Salinity-based**  

## Pickling / Depickling
Runs high pressure pump for a set period of time to fill the machine with pickling solution.  Also stores the pickled state in non-volatile memory in case of reboot.

## Error Handling
If any threshold fails after a configurable time period, the controller:
- Stops the machine
- Stores result code  
- Resets all valve states 
- Disables pumps  
- Logs result  
- Returns to IDLE

Error codes include membrane pressure failures, filter clogging, salinity issues, motor temperature, total flowrate loss, and more.
