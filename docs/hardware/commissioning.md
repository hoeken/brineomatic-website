---
layout: default
title: Commissioning
parent: Hardware
nav_order: 3
---

# Commissioning

Before testing each piece of hardware, you will need to configure it in **Settings -> Hardware**.  See the [Software Configuration]({{ '/docs/software/configuration' | relative_url }}) section for more information.

For the commissioning process, you will need to power Brineomatic from an external 12v or 24v power supply.

The easiest way to commission a system is to work through each sensor and actuator one by one, without connecting them to the watermaker.

## Step 1: Sensors

- **Flowmeters** you can test by blowing through them.
- **TDS sensors** you can test with a glass of tap water.
- **Pressure sensors** you can test simply by plugging in, as the system can detect valid 4-20ma sensor readings.
- **Temperature sensors** you can test by warming them up with your hand or a glass of hot water.

## Step 2: Relays / Solenoids

Switch to **MANUAL** mode and toggle the device you are testing.  Easy peasy.

## Step 3: Stepper Motor

The stepper motor can be tested by going to **Manual Mode -> Advanced**.  You can move it forwards and backwards.  Attach a piece of tape to the motor shaft to see it moving more easily.  Move it 360 degrees and make sure that is how far it moves to verify your stepper settings.

Once you have the stepper motor working, you can install it into the high pressure valve.  After that you should test again in manual mode to make sure that the set angle corresponds to the real world angle of the high pressure valve.  You should also check that the homing mode works correctly and doesnt jam in the open position.

## Step 4: Servo Motors

The servos can also be tested by going to **Manual Mode -> Advanced**.  You can move the servo to any arbitrary angle.  This will allow you to dial in the servo position for opening and closing valves.  Once you have the servo working, install it onto the valve assembly.  Now test the valve in Manual Mode by toggling the valve button itself, and not using the advanced mode.

## Step 5: Install Everything

Now that each individual portion of the system has been tested, you should install each piece onto the machine.  Be careful that you do not get any water on the electronics, and that you do not mix up any of the connectors.

## Step 6: Flush Valve Test

The first test, should be the flush valve.  This is a good test because it lets you test many other parts of the system without risking spraying high pressure water everywhere.  Enable the flush valve, and you should be able to see both your pressure sensors, brine tds, and brine flowrate sensors working.  Disable the valve and everything should go back to baseline.

## Step 7: High Pressure Pump

Once that is working, it is time to move on to the high pressure pump.  First, manually enable the high pressure pump.  Verify your flowrate and pressures are good.  Next, you can use your hand to manually rotate the pressure valve until your watermaker reaches the correct pressure.  Keep track of your rotations to come up with a rough guess the angle to program the stepper motor.

## Step 8: Diverter Valve

After a minute or two, the watermaker should be at pressure and producing good product water.  You can verify this will all of your sensors and any analog gauges you have installed.  Now you can test your diverter valve.  Make a note of your product, brine, and total flowrate.  Turn on the diverter valve button and the product water should go to your tanks. The total flowrate should also go down by the same amount as your product flowrate.  Turn the diverter valve off and it should go overboard with the brine.

## Step 9: High Pressure Valve

Open your high pressure valve and turn off your high pressure pump.  Use the Manual -> Advanced mode and click 'Home' on your stepper motor.  Verify that it moves in the correct direction and doesnt jam.  Use the UI to move it to your desired operating angle and verify it moves to that exact angle.  Use the homing button again to reset it.

Lastly, turn the high pressure pump on, and move your high pressure valve to your operating angle.  Use the +/- buttons to tweak the angle to get the pressure just right.  It is better to undershoot the pressure and slowly increase the angle so that you don't introduce backlash errors into the system.

## Step 10: Make Some Water!

Turn everything off, and now you are ready to [make some water]({{ '/docs/software/operation' | relative_url }})!