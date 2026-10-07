# Bill of Materials

**Electronics**

- CNC Shield, 1
- Arduino UNO Board / Compatible, 1
- Micro Limit Switch, 3
- DC Power Supply, 12V 3A, 1
- NEMA 17 Stepper Motor, 34/40mm, 2
- NEMA 17 Stepper Motor, 23mm, 1
- A4988 Stepper Driver, 3

**Mechanical**

- MGN15H Linear Rail with block, 500mm, 2
- Linear Rod 6mm, 150mm, 2
- Linear Bearing 6mm, 4
- GT2 Belt, 2m
- GT2 Tooth Pulley, 3
- GT2 Idler Pulley, 3
- Spacer Nuts
- Bolts and Nuts

**Compute**

- Raspberry Pi 5, 8GB, for the computer vision pipeline and path following logic

**Depth and force sensing**

- Distance/depth sensor for cutting depth: Depth Camera or VL53L5CX (or VL53L1X) Time of Flight sensor, with the analog IR sensor (GP2Y0A51SK0F) listed as budget fallback options if a depth camera or ToF module cannot be sourced
- Force Sensitive Resistor (FSR) or small load cell, mounted at the knife tip, for cutting force feedback

**Knife orientation axis**

- Positional servo (or a small closed loop stepper), replacing the SG90 continuous rotation servo from the base design, so the knife can hold a fixed angle during automatic cuts

**Manual mode controls**

- Joystick, for X and Y axis control
- Push button, for Z axis control
- Rotary knob, for knife rotation control

**Automatic mode controls**

- 12 digit keypad, for entering the target cutting depth
- Small LCD screen (I2C backpack recommended), for depth readout
