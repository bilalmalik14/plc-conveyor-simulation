# PLC Conveyor Motor Simulation

This project simulates a basic conveyor motor control system using **PLC ladder logic**, built on [PLC Fiddle](https://www.plcfiddle.com). It models real-world industrial behavior using start/stop control, a latching motor, and a sensor condition.

## 🔧 Project Overview

- When the **Start Button** is pressed, the **Motor** turns ON
- The Motor stays ON after Start is released (latch logic)
- When the **Stop Button** is pressed, the Motor turns OFF
- A simulated **Object Sensor** must be active for the Motor to run

This replicates the basic logic used in automation systems like conveyor belts, pumps, or industrial machines.

## 🧰 Components

- `Start_Button` (Normally Open)
- `Stop_Button` (Normally Closed)
- `Motor` (Output Coil)
- `Object_Sensor` (Normally Open)

## 🪜 Ladder Logic

```plaintext
[ Start_Button ]---+
                   |
[   Motor      ]---+----[/ Stop_Button ]----[ Object_Sensor ]----( Motor )
