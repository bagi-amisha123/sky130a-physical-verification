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

## Lab 3: Digital PLL LVS Exercise 6

### Source and files
Exercise files are under labs/lvs_exercise_6/, including the layout, Verilog sources, Netgen comparison script, and recorded output. See labs/lvs_exercise_6/README.md for exercise-specific provenance and instructions.

### Recorded result and limitations
The recorded Netgen comparison reports that the circuits match uniquely and Total errors = 0. The run also emitted warnings and placeholder-cell messages for some devices/modules. Treat this as the recorded exercise result, not as warning-free, sign-off-quality LVS or proof of silicon functionality. Review the exercise README and logs before drawing broader conclusions.

## Visual evidence
- screenshots/inverter_layout.png - PNG rendered from the inverter layout using KLayout image export.
- screenshots/drc_results.png - report-style graphic summarizing the two committed Magic DRC logs; this is not a Magic GUI screenshot.
- A PLL screenshot is not included because the KLayout batch export failed to parse the source .mag file. The source layout has not been modified to work around that issue.

## Repository structure
- labs/inverter/ - inverter layout, DRC script, and baseline log
- labs/drc_exercise_1/ - attributed reference DRC exercise and results
- labs/lvs_exercise_6/ - LVS exercise files, sources, script, and recorded output
- screenshots/ - available layout visual evidence
- docs/ - supporting documentation, if present

## Next steps
- Resolve the PLL layout-rendering compatibility issue without altering the original exercise source.
- Investigate the Netgen warnings and placeholder-cell messages before treating the LVS result as sign-off quality.
- Add further exercises with source attribution and reproducible logs.
