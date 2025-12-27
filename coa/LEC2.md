![[Screenshot 2025-12-26 at 4.28.55 PM.png]]

ALU has set of registers
1. general purpose
2. special purpose
WE WILL LOOK INTO SPECIAL REGISTERS IN PROCESSORS THIS LECTURE
![[Screenshot 2025-12-26 at 4.30.26 PM.png]]

special purpose regs: for interfacing with primary memory
Memory address register
this will hold address of memory location to be accessed
Memory data register
this will hold data to be written to memory/ to be read out memory

MEMORY IS JUST AN ARRAY OF STORAGE LOCATIONS WITH UNIQUE ADDRESSES

MAR: HOLDS MEMORY ADDRESS TO WRITE DATA TO THAT MEMORY/READ DATA OUT FROM THAT MEMORY, OR  HOLDS MEMORY ADDRESS TO READ INSTRUCTION FROM THAT MEMORY

MDR: HOLDS DATA TO WRITE TO MEMORY/READ DATA OUT FROM MEMORY, OR INSTRUCTION FROM THAT MEMORY

![[Screenshot 2025-12-26 at 5.11.53 PM.png]]

MAR holds the address here
MDR holds the data at each address here

![[Screenshot 2025-12-26 at 5.13.32 PM.png]]

MAR is connected with primary memory thru address bus
MDR is connected with primary memory thru data bus

why control signals?
	it will control whether to read or write
like for example if i want to read a data
	address is in MAR
	control signal will tell to read
	data gets stored in MDR

for example if i want to write a data
	address is in MAR
	data is in MDR
	control signal will tell to write
	data is written into the address in MAR to primary memory

![[Screenshot 2025-12-27 at 1.21.40 PM.png]]
![[Screenshot 2025-12-27 at 1.21.52 PM.png]]

For keeping track of the program:

there will be some counter that will point to a location and u will fetch and execute that instruction

![[Screenshot 2025-12-27 at 1.28.30 PM.png]]

![[Screenshot 2025-12-27 at 1.29.48 PM.png]]

PROGRAM COUNTER will contain the address for instruction to be executed
now we hv to store that somewhere
we will store it in INSTRUCTION REGISTER
![[Screenshot 2025-12-27 at 1.38.27 PM.png]]
we need to decode this instruction
![[Screenshot 2025-12-27 at 1.43.15 PM.png]]

if there are 4 bits for register address then there are 2^4/16 registers so we will specify one in them,here thats the case
there are 6 bits in opcode so there will be 2^6 operations/instructions
![[Pasted image 20251227134446.png]]

now we will see the architecture of the processor
![[Screenshot 2025-12-27 at 1.45.11 PM.png]]
**Concise, real-CPU view (what actually exists):**
### **Mandatory (logically present in** ### **all**###  **CPUs)**
- **PC** – next instruction
- **IR** – current instruction _(may be implicit)_
- **MAR / MDR** – memory interface _(often not programmer-visible)_
### **Programmer-visible (ISA-defined)**
- **General-purpose registers**
- **SP (stack pointer)**
- **Flags / Status register**
- **Control registers** (mode, interrupt, MMU)
### **Microarchitectural (hidden)**
- Pipeline registers
- Rename registers
- Load/store buffers
- Reorder buffer (OoO CPUs)

**Key insight:**
Modern CPUs **do not expose MAR/MDR explicitly**, but **functionally they exist**.

**One line:**
NPTEL shows a _conceptual CPU_; real CPUs have many more **hidden architectural + microarchitectural registers**.


so say an instruction states ADD R1,R2
those instructions are read by the ALU and it does the arithmetic operation and its stored back to those general purpose registers

![[Screenshot 2025-12-27 at 4.17.56 PM.png]]

here r1 and data at loca is addded and putin r1

![[Screenshot 2025-12-27 at 4.19.06 PM.png]]
![[Screenshot 2025-12-27 at 4.21.02 PM.png]]
![[Screenshot 2025-12-27 at 7.50.34 PM.png]]
![[Screenshot 2025-12-27 at 7.51.24 PM.png]]
![[Screenshot 2025-12-27 at 7.52.00 PM.png]]
![[Screenshot 2025-12-27 at 7.56.45 PM.png]]


![[Screenshot 2025-12-27 at 7.57.01 PM.png]]
![[Screenshot 2025-12-27 at 7.57.28 PM.png]]

### BUS ARCHITECTURE
![[Screenshot 2025-12-27 at 7.22.06 PM.png]]

so all these modules like processors, memory and i/o, so all these are communicating between each other
so they need a pathway, for communication

## Bus : group of lines that gives a connecting path

## there are some types of bus architectures like: single bus,multi-bus

### single bus:-
![[Screenshot 2025-12-27 at 7.29.51 PM.png]]

### so if the processor wants to talk to memory, it has to use this bus and no other modules will be using it at that moment

### there are buses inside processor like alu talks to registers
![[Screenshot 2025-12-27 at 7.40.24 PM.png]]![[Screenshot 2025-12-27 at 7.41.34 PM.png]]

### look into multi bus architecture



![[Screenshot 2025-12-27 at 7.43.34 PM.png]]