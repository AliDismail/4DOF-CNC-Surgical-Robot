# 4DOF CNC Surgical Robot

> **Status: Under Development**

A 4 degree of freedom CNC style robot (X, Y, Z, and knife rotation) with an orientable knife end effector, built to make controlled cuts by following a line drawn on the subject's surface, while maintaining a target cutting depth throughout the motion.

## Operating Modes

- **Manual**: a joystick drives X and Y, a button drives Z, and a knob controls knife rotation.
- **Automatic**: a target cutting depth is entered on a 12 digit keypad with a small LCD readout, the system scans a drawn line on the subject, and the robot follows it on its own while holding the requested depth.

## Project Documents

- `Base-Project-Credit.md`, credit for the base tutorial this project builds on, and what is being kept versus modified
- `Bill-Of-Materials.md`, full parts list, base tutorial parts plus the surgical specific additions
- `Brainstorming.md`, research notes covering actuation, depth and force sensing, line following, and control architecture

## Core Subsystems

- **Motion control**: Arduino Uno running GRBL, driving NEMA17 steppers through A4988 drivers
- **Knife axis**: positional servo (or small closed loop stepper), holding a fixed angle during automatic cuts
- **Depth and force sensing**: sensor fusion between a distance sensor and a force/pressure sensor at the knife tip
- **Vision and path following**: Raspberry Pi 5 running a computer vision pipeline to detect and follow the drawn line
- **ROS2**: running on the Raspberry Pi 5 for the vision, path planning, and serial bridge nodes

## Status Notes

This repository is an active work in progress. The mechanical base is being assembled first, with the surgical specific modifications layered on afterward.
