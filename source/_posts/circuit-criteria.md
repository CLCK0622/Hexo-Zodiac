---
title: Circuit Criteria
date: 2024-04-01 09:50:20
tags: docs
---
# Circuit Wiring Standards

## Circuit Planning

Consider "where the circuit comes from and where it goes."

### CAN Wires (22 AWG)

Start from the RoboRIO, connect all electrical components in series, and end at the PDH.

### High-Power Supply Wires (8-14 AWG)

Start from the PDH/PDP, directly connect to the electrical components.

- 12 AWG wire (standard for Falcon): If there is a power output, it must be connected to a **40 Amp** fuse.

- 14 AWG wire (if available): If there is a power output, it must be connected to a **30 Amp** fuse.

### Low-Power Supply Wires (18 AWG)

- Radio (field control) wire needs to be connected to the VRM (Voltage Regulator Module).

- RoboRIO should not be connected to the VRM.

- Limelight directly connects to the RoboRIO's 22 AWG power supply interface.

## Wiring

### Conduit

- At least 60% spare space must be reserved inside the conduit.
- There must be a fixing device every 0.5m inside the conduit.
- No quick-connect terminals are allowed inside the conduit.

### External Wiring

- Wiring should be horizontally and vertically aligned according to rigid structures.
- Wiring at corners should be near right angles; different vertical points should not be connected with slanted lines.
- Wire connection points should be centralized. Conduits should be used in long straight sections without connection points.
- Wires should not hang in the air and must be laid close to the surface.
- When using quick-connect terminals, do not press on the insulation layer; use a crimp terminal before inserting into the quick-connect terminal.

## Inspection

### Continuity

- CAN wires: Test the continuity of high (H) and low (L) level wires from the RoboRIO to the PDP/PDH with a multimeter.
- Power wires: Close the circuit breaker, test for short circuits from the PDP/PDH power supply end to the metal structure, then connect the power supply, and determine the power supply and CAN wire connection by observing the status lights.