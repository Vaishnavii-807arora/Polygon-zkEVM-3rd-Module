# Multiplier Circuit in CIRCOM
## Overview

This CIRCOM code defines a circuit template called Multiplier2, which checks whether the output signal c is the result of multiplying input signals a and b. The circuit uses custom gates for **AND**, **NOT**, and **OR** operations.

## Prerequisites
To understand and run the custom logic circuit, you will need the following:

* A basic understanding of digital logic and logic gates (AND, NOT, OR).
+ Any hardware description language (HDL) simulator that supports Verilog or VHDL.

# Circuit Description
## Input Signals
The Multiplier2 circuit template takes the following input signals:

**a**: Input signal representing the first operand.

**b**: Input signal representing the second operand.

## Intermediate Signals
The circuit creates two intermediate signals:

**x**: Result of the AND operation between signals a and b.

**y**: Result of the NOT operation on signal b.

## Output Signal
The final output signal is:

**q**: Result of the OR operation between signals x and y. It indicates whether c is the multiplication of a and b.

## Custom Gates
The circuit uses the following custom gates:

* **AND()**: Performs the logical AND operation between two input signals a and b.
* **NOT()**: Performs the logical NOT operation on the input signal in.
* **OR()**: Performs the logical OR operation between two input signals a and b.
  
## Circuit Logic
The logic of the **Multiplier2** circuit is as follows:

* The input signals **a** and **b** are connected to the input of the **AND** gate (andGate).
+ The output of the AND gate, **x**, is connected to one of the inputs of the **OR** gate (orGate).
- The input signal **b** is connected to the input of the **NOT** gate (notGate).
* The output of the NOT gate, **y**, is connected to the other input of the **OR** gate (orGate).
+ The output of the OR gate, **q**, represents whether c is the multiplication of **a** and **b**.


## Install
```
npm install
```
## Compile
```
npx hardhat circom
```
This will generate the out file with circuit intermediaries and geneate the MultiplierVerifier.sol contract
## Deploy
```
npx hardhat run scripts/deploy.ts
```

## How to Use
To use the Multiplier2 circuit in your HDL simulator, follow these steps:

1. Download the source code files from this repository.
2. Set up your HDL simulator and create a new project.
3. Add the source code files to the project.
4. Instantiate the Multiplier2 module in your testbench or main file.
5. Provide the inputs a and b to the Multiplier2 module.
6. Obtain the output Q from the Multiplier2 module to get the multiplication result.

## Author
Vaishnavi Arora

## License
This contract is licensed under the MIT License. SPDX-License-Identifier: MIT. 
