# SKY130A Physical Verification - Inverter Layout

## Overview
This submission documents a Magic-based design-rule check (DRC) of an inverter layout using the SkyWater SKY130A PDK.

## Tools
- Magic VLSI, version 8.3
- SkyWater SKY130A PDK
- OpenLane container environment

## Layout provenance
The inverter layout is derived from the public reference repository used for this exercise. It is not presented as an independently created layout.

## DRC procedure
The Tcl script is in labs/inverter/results/run_drc.tcl. The recorded output is in labs/inverter/results/drc_baseline.log.

## Recorded result
- Magic process exit code: 0
- Reported DRC errors: 0

This result applies to the layout and tool configuration used in the recorded run. It does not establish LVS correctness, circuit functionality, or sign-off readiness.

## Repository structure
- labs/inverter/layout/ - inverter layout and Magic configuration
- labs/inverter/results/ - DRC script and run logs
- docs/ - supporting documentation
- screenshots/ - visual evidence, when captured

## Next steps
- Capture layout and DRC screenshots.
- Perform an LVS comparison against a suitable reference netlist before claiming LVS success.
- Document additional checks and their results separately.
