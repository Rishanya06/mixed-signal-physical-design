
## Error Message
```md
[ERROR]: 5 errors found by linter
[ERROR]: Step 0 (verilator_lint_check) failed
%Error: /openlane/designs/design_mux/src/AMUX2_3V.v:10:9:
Duplicate declaration of signal: 'I0'

%Error: /openlane/designs/design_mux/src/AMUX2_3V.v:10:13:
Duplicate declaration of signal: 'I1'

%Error: /openlane/designs/design_mux/src/AMUX2_3V.v:11:9:
Duplicate declaration of signal: 'out'

%Error: /openlane/designs/design_mux/src/AMUX2_3V.v:12:9:
Duplicate declaration of signal: 'select'
```
## Problem

The OpenLane flow stopped during the linter stage before synthesis could begin.

## Investigation

The linter log was inspected to identify the source of the errors.

Multiple errors were traced back to the analog macro Verilog model (AMUX2_3V.v) and an incorrect signal connection inside design_mux.v.

## Root Cause

The analog macro file contained duplicate signal declarations and the top-level design referenced a non-existent signal named IO instead of I0.

## Fix
1.Removed duplicate signal declarations from AMUX2_3V.v.
2.Corrected the signal name IO → I0 in design_mux.v.

## Result

The linter completed successfully and the design progressed to synthesis.
