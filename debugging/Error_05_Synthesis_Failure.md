
---

# Error_05_Synthesis_Failure.md 
```md
## Error Message

[STEP 1]

[INFO]: Running Synthesis

[ERROR]: during executing yosys script

ERROR:
Re-definition of module '\spi_slave'
```
## Investigation

The synthesis log was analyzed using:
```md
grep -i "error" 1-synthesis.log
```
The error consistently pointed to duplicate compilation of the spi_slave module.

## Root Cause

The same spi_slave module was being read from two different sources.

## Fix

Removed the duplicate entry from config.json and reran the OpenLane flow.

## Result

The design successfully completed:

Synthesis
Floorplanning
Placement
CTS
Routing
Signoff

Final OpenLane Status:

[SUCCESS]: Flow complete.
