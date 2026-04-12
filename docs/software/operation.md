---
layout: default
title: Operation
parent: Software
nav_order: 3
---

# Operation

You can access the firmware at [http://brineomatic.local](http://brineomatic.local) ([http://brineomatic](http://brineomatic) on Android) or by entering the IP address.  The IP address and hostname are printed out over the serial port at startup.  You should see an interface similar to this:

![Brineomatic Idle]({{ 'assets/brineomatic-idle.png' | relative_url }})

## Normal Run Cycle

Supports three modes:
- **Automatic** (requires Tank Level data)
- **Duration**
- **Volume** (requires Brine Flowrate sensor)

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
- **Volume-based** (requires Brine Flowrate Sensor)
- **Automatic** (requires Brine TDS sensor)  

## Pickling / Depickling
Runs high pressure pump for a set period of time to fill the machine with pickling solution.  Also stores the pickled state in non-volatile memory in case of reboot or power loss.  Brineomatic can safely be turned off after entering Pickled mode and it will remember the state when you next turn it back on.

## Error Handling
If any threshold fails after a configurable time period, the controller:
- Stops the machine
- Stores result code  
- Resets all valve states 
- Disables pumps  
- Logs result
- Returns to IDLE

Error codes include membrane pressure failures, filter clogging, salinity issues, motor temperature, total flowrate loss, and more.