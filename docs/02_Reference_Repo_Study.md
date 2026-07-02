# Reference Repository Study

## Repository

Reference Repository:

https://github.com/praharshapm/vsdmixedsignalflow

---

## What the Repository Demonstrates

The repository demonstrates a mixed-signal physical design flow where a digital design integrates an analog macro and is implemented using OpenLane.

The complete flow includes:

1. RTL Design
2. Analog Macro Integration
3. Floorplanning
4. Placement
5. PDN Generation
6. Routing
7. DRC Verification
8. LVS Verification
9. Final GDS Generation

---

## Key Inputs

### Verilog

Defines the digital functionality.

Examples:

- design_mux.v
- raven_spi.v
- spi_slave.v

### LEF

Provides physical information about the analog macro.

Example:

- AMUX2_3V.lef

### PDK

The SKY130 open-source process design kit provides:

- Standard Cells
- Technology Rules
- Timing Libraries
- Physical Libraries

---

## My Understanding

Before this project I had limited exposure to physical design flows.

Studying the repository helped me understand how:

- RTL becomes a physical layout
- Analog macros are integrated into digital designs
- OpenLane automates the RTL-to-GDS flow
- Timing and manufacturability checks are performed