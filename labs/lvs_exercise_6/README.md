# SKY130A LVS Exercise 6 — Digital PLL

## Overview
This exercise compares the Magic-extracted `digital_pll.spice` netlist with the `digital_pll` Verilog netlist using Netgen and the SKY130A setup file.

## Source and attribution
Reference-derived educational exercise:
https://github.com/yathAg/Physical_Verification_SKY130A

The included source files and original run script are retained with attribution. The Netgen setup path and helper-script path were adjusted for the local container environment.

## Reproduce
From the `netgen` directory, run:

    sh run_lvs.sh

## Observed result
- Final result: `Circuits match uniquely.`
- Total errors: `0`
- Netgen reports no net, device, pin, or property mismatches.

## Limitations
The run emitted undefined-subcircuit warnings and created placeholder cell definitions for some devices/modules. This is a successful Netgen comparison under the supplied setup, not a claim of warning-free, signoff-quality LVS verification.

## Tools
- Magic
- Netgen
- SKY130A PDK
