# ARM LEGv8 CPU

LEGv8 is a simple version of ARMv8 defined and used in the book Computer Organization and Design - The Hardware/Software Interface ARM Edition by David A. Patterson and John L. Hennessy.

[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/nextseto/ARM-LEGv8/master/LICENSE)

This repository contains the source code for an ARM LEGv8 CPU written in Verilog.

Supported instructions include: `LDUR`, `STUR`, `ADD`, `SUB`, `ORR`, `AND`, `CBZ`, `B`, and `NOP`.

This CPU is based on the ARM architecture from the textbook: *Computer Organization and Design: The Hardware/Software Interface ARM Edition by D. Patterson and J. Hennessy, Morgan Kaufmann, 2016* [ISBN: 978-012-8017333](https://www.amazon.com/Computer-Organization-Design-Interface-Architecture/dp/0128017333/ref=sr_1_1?ie=UTF8&qid=1483051663&sr=8-1&keywords=9780128017333)

## Versions

- [Single-Cycle](/Single-Cycle): Simulates an ARM LEGv8 single-cycle CPU

- [Pipelined-Only](/Pipelined-Only): Simulates an ARM LEGv8 multi-cycle/pipelined CPU

- [Pipelined with Hazard Detection and Forwarding Unit](/Pipeline-With-Hazard-And-Forwarding): Simulates an ARM LEGv8 multi-cycle/pipelined CPU with hazard detection and forwarding capabilities

## Assembler

`legv8_asm.py` is an assembler that converts ARM LEGv8 assembly into machine code (binary and hex).

##### Example

```
Enter an ARM LEGv8 Instruction: LDUR x10 [x1, #10]

------- C Interpretation -------
Register[10] = RAM[ Register[1] + 10 ]

------- Machine Code (32-bits) -------
BINARY : 11111000010000001010000000101010
HEX    : f840a02a
```

## To Simulate

There are two ways to run and simulate the projects below. Either use the **Xilinx Vivado** or an online tool called **EDA Playground**.

##### Option 1. Xilinx Vivado

- Run the Xilinx Vivado Suite with the module and testbench files for each project. More instructions can be found [here](https://www.xilinx.com/support/university/students.html#overview).

##### Option 2. [EDA Playground](http://www.edaplayground.com/home)
- Login with a Google or Facebook account to save and run modules and testbenches
- Testbench + Design: SystemVerilog/Verilog
- Tools & Simulators: Icarus Verilog 0.9.7

## Credits

- [Ralph Quinto](https://github.com/RakiRoad)
- Nikita Eisenhauer

## License

All source code in **ARM-LEGv8** are released under the MIT license. See LICENSE for details.
