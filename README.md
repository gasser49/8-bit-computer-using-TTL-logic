# 8-bit-computer-using-TTL-logic
OVERVIEW
This project is a manually controlled 8-bit computer using TTL logic ICs on breadboard. The goal was to build a fully functioning computer that works at a hardware level.

The computer was designed, wired, tested and debugged manually. While using external resources(Ben Eater’s 8-bit computer series) as a technical reference to verify wiring and avoid damaging components.

The control unit is not microcoded; instead, the computer is operated through manual control signal to each execution.

SYSTEM ARCHITECTURE
Core Components:
    8-bit data bus
    Register A and Register B
    ALU capable of addition and subtraction
    RAM module for data storage 
    Instruction register
    Program counter
    Output display module
Control:
    No EEPROM microcode
    Control signals are manually asserted
Clock System:
    Discrete clock circuit
    Manual and automatic modes

BUILD PROCESS
Built over two weeks
About 6 hours daily 
Each module was:
    designed
    wired
    tested
    verified before integration
Most subsystems function reliably on their own. However, when fully integrated, intermittent instability appears.

TECHNICAL CHALLENGES AND DEBUGGING
the only challenge faced me was the system instability when all modules were connected together. After observation I concluded that:
    The clock starts normally, then becomes unstable
    Random behavior unless slight pressure or board adjustment was applied

Investigated causes:
    breadboard contact resistance 
    Signal noise and long clock lines 
    IC quality inconsistencies (local component availability)

Mitigation Attempts to solve it:
    Decoupling capacitors on every IC
    Shortened clock wiring
    Clock buffering
    Replacing clock IC
    RE-testing modules individually (all passed)

Despite all this effort the issue remained under full integration, leading to the conclusion that component quality and breadboard limitations were the primary causes 

USE OF EXTERNAL REFERENCES 
Ben Eater’s 8-bit computer series was used as:
    A conceptual reference
    A wiring verification guide to prevent damage 
Only one submodule(the display unit) follows the reference design after an EEPROM was damaged during experimentation. this decision was made due to component cost.

WHAT THIS PROJECT DEMONSTRATES 
understanding of:
    Digital logic
    Data bus
    Registers and ALU operation and design
    Clock distribution

The ability to learn complex systems

LIMITATIONS AND FUTURE WORK
Current limitation:
    No automated control unit(microcoded control unit)
    intermittent instability under full system integration

Future improvements:
    PCB-based version of the 8-bit computer
    Microcoded control unit using EEPROM

AUTHOR
High school student (Thanawya Amma/Grade 11)
Aspiring to be a Computer Engineer

LICENSE
Educational / personal project