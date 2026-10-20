# SKY130A DRC Exercise 1

## Objective
Explore the Magic layout and design-rule-checking workflow using the SKY130A technology.

## Source and attribution
The layout and Magic technology configuration are copied from the Lab 3 DRC Exercise 1 materials in:
https://github.com/yathAg/Physical_Verification_SKY130A

The layout is a reference workshop exercise, not an independently designed layout.

## Files
- `layout/exercise_1.mag` - reference layout.
- `layout/.magicrc` - Magic SKY130A configuration.
- `layout/run_drc.tcl` - commands used to run DRC.
- `results/drc_exercise_1.log` - captured tool output.

## Verification environment
- Magic: 8.3 revision 413
- Technology: SKY130A
- Technology version reported by Magic: `1.0.493-0-g0fe599b`

## Result
The recorded run loaded `exercise_1.mag` and reported:

`Total DRC errors found: 0`

This result applies to this layout and this run configuration only. It does not establish LVS correctness or verify every SKY130A design rule.

## Reproduce
From the `layout` directory, run:

```sh
magic -dnull -noconsole -rcfile .magicrc < run_drc.tcl
```

The command's output can be redirected to a log file when rerunning the check.
