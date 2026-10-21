# SKY130A Physical Verification

## Overview

This repository records physical-verification experiments using the
SKY130A process design kit (PDK), Magic VLSI, and Netgen.

The repository distinguishes tool-execution evidence from original
circuit/layout design. Reference-derived exercise files are not claimed
as independently designed work.

## Tools

- Magic VLSI 8.3
- SkyWater SKY130A PDK
- Netgen LVS
- OpenLane container environment

## Exercise 1: Inverter DRC

**Purpose:** Run Magic design-rule checking on the inverter layout.

- Layout: `labs/inverter/layout/inverter.mag`
- DRC script: `labs/inverter/results/run_drc.tcl`
- Recorded log: `labs/inverter/results/drc_baseline.log`

**Recorded result:** The log reports `Total DRC errors found: 0`.

The inverter layout is derived from a public reference repository.
This result applies only to the tested layout and recorded configuration;
it does not establish circuit functionality, LVS correctness, or
manufacturing sign-off readiness.

## Exercise 2: DRC Exercise 1

**Purpose:** Examine a SKY130A layout and run the Magic DRC workflow.

- Layout: `labs/drc_exercise_1/layout/exercise_1.mag`
- Magic configuration: `labs/drc_exercise_1/layout/.magicrc`
- Script: `labs/drc_exercise_1/layout/run_drc.tcl`
- Log: `labs/drc_exercise_1/results/drc_exercise_1.log`
- Notes: `labs/drc_exercise_1/README.md`

The layout and configuration are copied from Lab 3, Exercise 1 of
the public reference repository:
https://github.com/yathAg/Physical_Verification_SKY130A

**Recorded result:** The log reports `Total DRC errors found: 0`.

This is a recorded result for the supplied exercise, not proof that every
design rule or every SKY130A layout has been checked.

## Exercise 3: Digital PLL LVS Exercise 6

**Purpose:** Compare the layout and schematic/netlist representations
using the provided Netgen LVS flow.

- Exercise notes: `labs/lvs_exercise_6/README.md`
- Layout and related files: `labs/lvs_exercise_6/mag/`
- Verilog sources: `labs/lvs_exercise_6/verilog/`
- Comparison script: `labs/lvs_exercise_6/netgen/run_lvs.sh`
- Recorded log: `labs/lvs_exercise_6/netgen/lvs.log`

**Recorded result:** The log reports a unique circuit match and
`Total errors = 0`. It also contains warnings and placeholder-cell
messages that require further investigation. This should not be
interpreted as warning-free, sign-off-quality LVS or proof of silicon
functionality.

## Evidence

- `screenshots/inverter_layout.png` - layout image exported using KLayout.
- `screenshots/drc_results.png` - report-style summary of the recorded
  DRC logs; it is not a screenshot of the Magic application.

These images are supplementary. The raw logs and scripts are the primary
evidence of the recorded tool runs.

## Limitations and next steps

- Investigate Netgen warnings and placeholder-cell messages.
- Resolve the PLL layout-rendering compatibility issue.
- Create an independently designed layout and verify it from a documented
  starting point.
- Capture genuine tool screenshots and preserve reproducible commands,
  tool versions, and raw outputs.

## Scope and attribution

Some exercise layouts and source files are reference-derived. Their
provenance is documented in the relevant exercise notes where available.
The repository records verification runs and their observed outputs;
it does not claim that every included design was created independently.
## Latest Verification Evidence

### SKY130A Design Rule Checking

- **Tool:** Magic 8.3, revision 413
- **Technology:** SKY130A, version 1.0.493
- **Layout:** `labs/drc_exercise_1/layout/exercise_1.mag`
- **Execution log:** `labs/drc_exercise_1/results/drc_run.log`
- **Recorded result:** 0 DRC errors

The result applies to this exercise layout and recorded run only. It does not establish full-chip signoff.

### Other Exercises

- Inverter DRC: `labs/inverter/results/drc_baseline.log`
- PLL LVS: `labs/lvs_exercise_6/netgen/lvs.log`

Review the LVS log alongside its documented placeholder-cell warnings and limitations.

