## Error Message

%Error: /openlane/designs/design_mux/src/AMUX2_3V.v:10:9:
Duplicate declaration of signal: 'I0'

%Error: /openlane/designs/design_mux/src/AMUX2_3V.v:10:13:
Duplicate declaration of signal: 'I1'

%Error: /openlane/designs/design_mux/src/AMUX2_3V.v:11:9:
Duplicate declaration of signal: 'out'

%Error: /openlane/designs/design_mux/src/AMUX2_3V.v:12:9:
Duplicate declaration of signal: 'select'

## Problem

The custom analog macro AMUX2_3V could not be integrated cleanly into the OpenLane flow.
Investigation

The analog macro Verilog model was inspected and compared with its module port declaration.

Root Cause

The signals were declared twice.

Example:
input I0;
input I1;
output out;
input select;

wire I0;
wire I1;
wire out;
wire select;

The ports already define the signals. Redeclaring them as wires caused Verilator to report duplicate declarations.
Fix

Removed the redundant wire declarations.

Result

The analog macro was successfully recognized by OpenLane and the linter errors were eliminated.
