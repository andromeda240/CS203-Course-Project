# Simple Hash Function Using XOR & Bitwise Shifts

## Overview
This project implements a simple hash function in Verilog HDL, compressing a 16-bit input into an 8-bit hash digest using XOR, bitwise shifts, rotations, and an S-box substitution. It demonstrates basic combinational logic techniques for effective data mixing and diffusion, suitable for educational purposes in digital system design.

## Features
- 16-bit input split into two 8-bit halves and mixed with XOR.
- Bitwise rotations and shifts for bit diffusion.
- Keyed hash mixing for increased security.
- 4-bit S-box substitution introducing non-linearity and avalanche effect.
- Pure combinational design with no memory elements.
- Tested with diverse input patterns to verify robustness.
- Histogram analysis for uniform distribution and low collision.

## Design Summary
- Single Verilog module implementing the hash logic.
- Testbench covers all 65,536 possible 16-bit inputs.
- Output waveforms demonstrate strong diffusion and avalanche behavior.

## How to Compile & Simulate

Run these commands in your terminal to compile, simulate, and view waveforms(Icarus Verilog):
```sh
iverilog -o simv tb.v code.v && vvp simv
gtkwave SimpleHash.vcd &
