# SR Latch Using NAND Gates (Verilog HDL)

## Overview

This project implements an **SR (Set-Reset) Latch** using cross-coupled NAND gates in Verilog HDL. The SR latch is one of the fundamental sequential logic circuits used for storing a single bit of information.

## Features

* Verilog HDL implementation
* Cross-coupled NAND gate realization
* Functional simulation testbench
* Demonstrates Set, Reset, Hold, and Invalid states
* Compatible with Xilinx Vivado

## Circuit Description

The SR latch consists of two NAND gates connected in a feedback configuration.

Equations:

Q = ~(S & Qbar)

Qbar = ~(R & Q)

Inputs are active LOW:

* S = 0 → Set
* R = 0 → Reset
* S = 1 and R = 1 → Hold
* S = 0 and R = 0 → Invalid State

## Verilog Module

File: `sr_latch01.v`

The module implements an SR latch using continuous assignments and NAND logic.

## Testbench

File: `sr_latch01_stimuli.v`

The testbench verifies:

1. Set Operation
2. Hold Operation
3. Reset Operation
4. Hold Operation
5. Invalid State

## Truth Table

| S | R | Q(next) | Qbar(next) | Operation |
| - | - | ------- | ---------- | --------- |
| 1 | 1 | Hold    | Hold       | Memory    |
| 0 | 1 | 1       | 0          | Set       |
| 1 | 0 | 0       | 1          | Reset     |
| 0 | 0 | 1       | 1          | Invalid   |

## Simulation Results

Simulation waveforms confirm the correct operation of the SR latch for all valid input combinations.

## Tools Used

* Verilog HDL
* Xilinx Vivado
* GitHub

## Learning Outcomes

* Understanding sequential circuits
* Cross-coupled feedback structures
* Active-low control inputs
* Verilog HDL modeling
* Testbench development and verification

## Author

Neeraj Yadav

M.Tech (Research)

IIT Dharwad
