# 8-bit Computer Using TTL Logic

## Overview

This project is a manually controlled 8-bit computer using TTL logic ICs on breadboard. The goal was to build a fully functioning computer that works at a hardware level.

The computer was designed, wired, tested and debugged manually while using external resources (Ben Eater's 8-bit computer series) as a technical reference to verify wiring and avoid damaging components.

The control unit is not microcoded; instead, the computer is operated through manual control signals for each execution.

## Video documentation (wiring, testing)
- https://youtube.com/playlist?list=PLksuvnj3mpLGEFsioQ8tjdo8dZZ7gaVC_&si=0-ix42xb5nYniTDr

## System Architecture

### Core Components
- 8-bit data bus
- Register A and Register B
- ALU capable of addition and subtraction
- RAM module for data storage
- Instruction register
- Program counter
- Output display module

### Control
- No EEPROM microcode
- Control signals are manually asserted

### Clock System
- Discrete clock circuit
- Manual and automatic modes

## Build Process

- **Duration**: Built over two weeks at about 6 hours daily
- **Process**: Each module was designed, wired, tested, and verified before integration

Most subsystems function reliably on their own. However, when fully integrated, intermittent instability appears.

## Technical Challenges and Debugging

The primary challenge was system instability when all modules were connected together. After observation, the following was concluded:

### Symptoms
- The clock starts normally, then becomes unstable
- Random behavior unless slight pressure or board adjustment was applied

### Investigated Causes
- Breadboard contact resistance
- Signal noise and long clock lines
- IC quality inconsistencies (local component availability)

### Mitigation Attempts
- Decoupling capacitors on every IC
- Shortened clock wiring
- Clock buffering
- Replacing clock IC
- Re-testing modules individually (all passed)

Despite these efforts, the issue remained under full integration, leading to the conclusion that component quality and breadboard limitations were the primary causes.

## Use of External References

Ben Eater's 8-bit computer series was used as:
- A conceptual reference
- A wiring verification guide to prevent damage

Only one submodule (the display unit) follows the reference design after an EEPROM was damaged during experimentation. This decision was made due to component cost.

## What This Project Demonstrates

### Understanding of:
- Digital logic
- Data bus
- Registers and ALU operation and design
- Clock distribution
- The ability to learn complex systems

## Limitations and Future Work

### Current Limitations
- No automated control unit (microcoded control unit)
- Intermittent instability under full system integration

### Future Improvements
- PCB-based version of the 8-bit computer
- Microcoded control unit using EEPROM

## Author

High school student (Thanawya Amma/Grade 11)  
Aspiring to be a Computer Engineer

## License

Educational / personal project
