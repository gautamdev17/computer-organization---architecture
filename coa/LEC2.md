![[Screenshot 2025-12-26 at 4.28.55 PM.png]]

ALU has set of registers
1. general purpose
2. special purpose
WE WILL LOOK INTO SPECIAL REGISTERS IN ALU THIS LECTURE
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