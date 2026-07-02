
---

# docs/04_Analog_Macro_Study.md

```md
# Analog Macro Study

## What is an Analog Macro?

An analog macro is a pre-designed analog block that is integrated into a larger digital system.

Examples include:

- ADCs
- DACs
- PLLs
- Multiplexers

---

## Analog Macro Used

Macro:

AMUX2_3V

Function:

2:1 Analog Multiplexer

Inputs:

- I0
- I1

Control:

- select

Output:

- out

---

## Why LEF is Needed

The Verilog model describes functionality.

The LEF file describes:

- Physical dimensions
- Pin locations
- Placement information

Without the LEF file OpenLane cannot place the analog block during floorplanning.

---

## Integration Process

The analog macro was added through:

- AMUX2_3V.v
- AMUX2_3V.lef

The LEF was included in config.json using:

EXTRA_LEFS

This allowed OpenLane to recognize and place the analog macro correctly.