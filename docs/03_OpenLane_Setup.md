# OpenLane Setup

## Environment

Tool Used:

- OpenLane
- SKY130A PDK
- Docker Container

---

## Design Setup

A new OpenLane design directory was created.

Files added:

- design_mux.v
- raven_spi.v
- spi_slave.v
- AMUX2_3V.v
- AMUX2_3V.lef

---

## Configuration

The config.json file was updated to include:

- Verilog sources
- Analog macro LEF
- Clock settings
- Floorplan settings

Example:

- CLOCK_PORT = SCK
- CLOCK_PERIOD = 10 ns

---

## Running the Flow

The flow was executed using:

```bash
./flow.tcl -design design_mux