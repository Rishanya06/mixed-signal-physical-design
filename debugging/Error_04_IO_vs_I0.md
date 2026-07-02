
---

# Error_04_Duplicate_spi_slave.md

This is one of the biggest debugging steps you did.

```md
## Error Message

/openlane/designs/design_mux/src/spi_slave.v:53:

ERROR: Re-definition of module '\spi_slave'
Generating RTLIL representation for module '\spi_slave'.

3. Executing Verilog-2005 frontend:
/openlane/designs/design_mux/src/spi_slave.v

ERROR: Re-definition of module '\spi_slave'

Investigation

The top-level module instantiation was reviewed.

Root Cause

A typographical error was found:

.I0(IO)

The letter O was used instead of the digit 0.

Fix

Corrected the connection:

.I0(I0)
Result

The warning disappeared and the intended signal was connected correctly.