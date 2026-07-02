
---

# Error_03_IO_vs_I0.md

This came directly from your linter output.

```md
## Error Message

%Warning-IMPLICIT:
/openlane/designs/design_mux/src/design_mux.v:31:8:

Signal definition not found,
creating implicitly: 'IO'

Suggested alternative: 'I0'

## Problem

OpenLane failed during synthesis because the spi_slave module was being compiled more than once.

Generating RTLIL representation for module '\spi_slave'.

3. Executing Verilog-2005 frontend:
/openlane/designs/design_mux/src/spi_slave.v

ERROR: Re-definition of module '\spi_slave'

Investigation

The synthesis log was inspected to determine where the duplicate module was being introduced.

Root Cause

The spi_slave module already existed inside raven_spi.v.

At the same time, spi_slave.v was also listed separately inside config.json:

"dir::src/spi_slave.v"

As a result, Yosys attempted to compile the same module twice.

Fix

Removed spi_slave.v from the VERILOG_FILES list in config.json.

Result

The duplicate module issue was resolved and synthesis proceeded successfully.