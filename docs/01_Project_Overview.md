# Project Overview

## Objective

The goal of this project was to understand the complete mixed-signal physical design flow using open-source EDA tools.

As part of the VSD AI Mixed Signal Internship task, I studied the reference repository and reproduced a similar RTL-to-GDS implementation using OpenLane and the SKY130 PDK.

Instead of simply following the repository, I used an AI-assisted workflow to understand each stage, debug errors, verify results, and document the complete process.

---

## What Was Studied

The project focused on:

- Mixed-signal physical design fundamentals
- Analog macro integration
- LEF/LIB/Verilog usage
- OpenLane flow configuration
- Floorplanning
- Placement
- Power Distribution Network (PDN)
- Routing
- DRC and LVS verification
- Final GDS generation

---

## Design Used

The design contains:

- SPI interface
- SPI slave controller
- Analog 2:1 multiplexer macro (AMUX2_3V)

Files used:

- design_mux.v
- raven_spi.v
- spi_slave.v
- AMUX2_3V.v
- AMUX2_3V.lef

---

## Final Outcome

The OpenLane flow completed successfully and generated:

- GDSII Layout
- DEF
- LEF
- Netlists
- Timing Reports
- Manufacturability Reports

The final design achieved:

- DRC Clean Layout
- LVS Clean Verification
- Successful Analog Macro Integration