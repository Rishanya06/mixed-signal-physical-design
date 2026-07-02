# Key Learnings

## Mixed-Signal Physical Design

This project helped me understand how digital and analog blocks can coexist in a single chip design. The analog multiplexer was integrated into the OpenLane flow using LEF and Verilog wrapper files.

## OpenLane Flow Understanding

I gained hands-on experience with:

- Synthesis
- Floorplanning
- Placement
- Clock Tree Synthesis
- Routing
- DRC Verification
- LVS Verification
- GDS Generation

## Analog Macro Integration

I learned that analog blocks are not synthesized like standard digital logic. Instead, they are integrated as hard macros using LEF and abstract physical information.

## Debugging Experience

Several implementation issues were encountered:

- Missing AMUX2_3V module
- Duplicate spi_slave module definitions
- Incorrect signal naming (IO vs I0)
- Configuration file syntax errors
- OpenLane synthesis failures

Each issue was debugged and resolved step by step.

## AI-Assisted Workflow

ChatGPT was used to:

- Understand the reference repository
- Break the project into smaller tasks
- Generate debugging strategies
- Explain OpenLane reports
- Assist in documenting results

All generated suggestions were manually verified before use.

## Future Improvements

Possible next steps include:

- Running custom DRC analysis
- Exploring larger mixed-signal designs
- Integrating additional analog IPs
- Performing power and timing optimization