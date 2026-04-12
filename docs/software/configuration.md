---
layout: default
title: Configuration
parent: Software
nav_order: 3
---

# Configuration

## Hardware

{: .note }
For all actuators with "MANUAL" mode: when this is selected, Brineomatic will still output the desired state of the hardware to the API and MQTT.  This allows you to control hardware indirectly through something MQTT, Home Assisant, or your own custom solution.  Of course you can also just manually flip a switch if needed as well.

### Boost Pump

The boost pump is a low pressure pump that supplies the high pressure pump with water.  It gets turned on before the high pressure pump runs and off after it finishes.

- NONE - Not installed, Brineomatic will skip all related operations.
- MANUAL - Boost Pump present, but controlled externally.
- RELAY - Boost Pump controlled by relay, with configurable channel.

**Inverted** - Tells Brineomatic whether ON or OFF provides power to the relay.
**After Turn On Delay** - a programmable delay to allow flow to stabilize before turning on the high pressure pump.

### High Pressure Pump

- NONE - Not installed, Brineomatic will skip all related operations.
- MANUAL - High Pressure Pump present, but controlled externally.
- RELAY - High Pressure Pump controlled by relay, with configurable channel.
- MODBUS - High Pressure Pump controlled by VFD over MODBUS, configurable below.

**Inverted** - Tells Brineomatic whether ON or OFF provides power to the relay.
**After Turn On Delay** - a programmable delay to allow flow to stabilize before starting the safety checks.

### High Pressure Valve

- NONE - Not installed, Brineomatic will skip all related operations.
- MANUAL - High Pressure Valve present, but controlled externally.
- STEPPER - High Pressure Valve controlled by stepper motor

**Step Angle** - Degrees per step.  Most NEMA17 stepper motors are 1.8°, but 0.9° versions do exist.
**Gear Ratio** - Gear ratio used to calculate the steps per angle of the high pressure valve.
**High Pressure Valve Close** - Speed and angle to move the High Pressure valve to its high pressure operating position.
**High Pressure Valve Open** - Speed and angle to move the High Pressure valve to its low pressure "off" position.
**Stepper Motor Current** - Percentage of current to deliver to the stepper motor (~1.7A at 100%)  It is best to keep this as low as possible without losing steps to keep the stepper motor and driver from overheating.  Home current is used during homing and should be lower than Run current so that homing does not get the valve stuck.

### Diverter Valve

- NONE - Not installed, Brineomatic will skip all related operations.
- MANUAL - Diverter Valve present, but controlled externally.
- RELAY - Diverter Valve controlled by relay, with configurable channel.
- SERVO - Diverter Valve controlled by servo, configurable below.

**Inverted** - Tells Brineomatic whether ON or OFF provides power to the relay.
**Open and Close Angles** - In SERVO mode, these are the angles to move the servo to.  You can pull these values directly from Manual -> Advanced mode.

### Flush Valve

- NONE - Not installed, Brineomatic will skip all related operations.
- MANUAL - Flush Valve present, but controlled externally.
- RELAY - Flush Valve controlled by relay, with configurable channel.
- SERVO - Flush Valve controlled by servo, configurable below.

**Inverted** - Tells Brineomatic whether ON or OFF provides power to the relay.
**Open and Close Angles** - In SERVO mode, these are the angles to move the servo to.  You can pull these values directly from Manual -> Advanced mode.

### Cooling Fan

- NONE - Not installed, Brineomatic will skip all related operations.
- MANUAL - Flush Valve present, but controlled externally.
- RELAY - Flush Valve controlled by relay, with configurable channel.

**Inverted** - Tells Brineomatic whether ON or OFF provides power to the relay.
**ON / OFF Temperature** - The cooling fan will be turned on and off based on the motor temperature.

### Pressure Sensors

**Min / Max Pressure** - 4-20ma pressure transducers are rated for a pressure range.  Simply enter that into the configuration.

### Flowrate Sensors

**Pulses Per Liter** - The number of pulses per liter.  If your flowmeter has a rated *frequency*, then simply multiply that by 60 to get pulses per liter.

### TDS Sensors

**Calibration Offset** - After a TDS reading is made, this number will be added to the reading to calculate the true TDS.

### Temperature Sensors

- NONE - Not installed, Brineomatic will skip all related operations.
- EXTERNAL - Temperature data provided through Brineomatic API
- DS18B20 - Temperature sensor present, connected to Brineomatic
- MQTT - Temperature data pulled from MQTT topic

**MQTT Path** - The MQTT path to the temperature.  Units should be in Celcius

### Tank Level

- NONE - Not installed, Brineomatic will skip all related operations.
- EXTERNAL - Tank level data provided through Brineomatic API
- MQTT - Tank level data pulled from MQTT topic

**MQTT Path** - The MQTT path to the tank level data.  Can either be 0.0-1.0 or 0-100%.

### Battery Level

- NONE - Not installed, Brineomatic will skip all related operations.
- EXTERNAL - Battery level data provided through Brineomatic API
- MQTT - Battery level data pulled from MQTT topic

**MQTT Path** - The MQTT path to the battery level data.  Can either be 0.0-1.0 or 0-100%.