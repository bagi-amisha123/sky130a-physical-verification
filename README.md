# SKY130A Physical Verification

## Overview
This repository documents Magic-based design-rule checking (DRC) experiments using the SkyWater SKY130A PDK.

## Tools
- Magic VLSI, version 8.3
- SkyWater SKY130A PDK
- OpenLane container environment

## Lab 1: Inverter Layout

### Layout provenance
The inverter layout is derived from a public reference repository used for this exercise. It is not presented as an independently created layout.

### DRC procedure
- Script: `labs/inverter/results/run_drc.tcl`
- Recorded output: `labs/inverter/results/drc_baseline.log`

### Recorded result
- Magic process exit code: 0
- Reported DRC errors: 0

This result applies to the layout and tool configuration used in the recorded run. It does not establish LVS correctness, circuit functionality, or sign-off readiness.

## Lab 2: DRC Exercise 1

### Objective
Explore a reference layout and the Magic DRC workflow with SKY130A.

### Source and attribution
The layout and Magic configuration are copied from Lab 3, Exercise 1 of:
https://github.com/yathAg/Physical_Verification_SKY130A

This is an attributed reference exercise, not an independently designed layout.

### Files
- `labs/drc_exercise_1/layout/exercise_1.mag` - reference layout
- `labs/drc_exercise_1/layout/.magicrc` - Magic SKY130A configuration
- `labs/drc_exercise_1/layout/run_drc.tcl` - DRC commands
- `labs/drc_exercise_1/results/drc_exercise_1.log` - recorded output
- `labs/drc_exercise_1/README.md` - exercise documentation

### Recorded result
Magic loaded `exercise_1.mag` using SKY130A and reported:

`Total DRC errors found: 0`

This result applies only to this layout and recorded configuration. It does not establish LVS correctness or verify every SKY130A rule.

## Repository structure
- `labs/inverter/` - inverter layout, DRC script, and baseline log
- `labs/drc_exercise_1/` - attributed reference DRC exercise and results
- `docs/` - supporting documentation
- `screenshots/` - visual evidence, when captured

## Next steps
- Capture layout and DRC screenshots.
- Perform an LVS comparison against a suitable reference netlist before claiming LVS success.
- Add further DRC exercises separately, with source attribution and reproducible logs.
