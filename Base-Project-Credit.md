# Base Project Credit

This project uses the **DIY Pen Plotter with Automatic Tool Changer** by Dejan at How To Mechatronics as its mechanical and electronic base.

Original tutorial: https://howtomechatronics.com/projects/diy-pen-plotter-with-automatic-tool-changer-cnc-drawing-machine/

Original 3D model and STL files: https://cults3d.com/en/3d-model/tool/diy-cnc-pen-plotter-with-automatic-tool-color-change

## What is being kept from the base design

- The X and Y axis motion system, using MGN15H linear rails with GT2 belts and pulleys
- The Arduino Uno, CNC Shield, and A4988 stepper driver setup running GRBL firmware
- The three axis homing approach using micro limit switches
- The general reciprocating Z axis mechanism (sliding on linear rods with linear bearings)

## What will be modified for this project

This base design is being adapted from a pen plotter into a 3DOF CNC style surgical robot for testing controlled cuts on soft material (playdough shaped like tissue), following a drawn line while maintaining a target cutting depth. The following parts of the original design are being changed or replaced:

- The pen gripper and automatic pen holder mechanism will be removed and replaced with an orientable knife end effector
- The knife orientation axis will use a positional servo (or a small closed loop stepper) instead of the SG90 continuous rotation servo used for the pen gripper, since the knife needs to hold a fixed angle during automatic cuts
- The Z axis will be extended to support a sensor fusion depth control loop, combining a force/pressure sensor and a distance sensor (originally planned as a depth camera, with budget friendly ToF or analog IR alternatives also being considered)
- A manual control mode will be added, using a joystick for X and Y, a button for Z, and a knob for knife rotation
- An automatic mode will be added, using a 12 digit keypad and small LCD for entering a target cutting depth, combined with a computer vision line following system to track a drawn line on the test material
- GRBL will continue to run on the Arduino for real time motion control, but a Raspberry Pi 5 will be added to handle the computer vision pipeline and path following logic, communicating with the Arduino over serial
