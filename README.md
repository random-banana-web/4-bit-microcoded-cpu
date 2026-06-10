# 4-bit-microcoded-cpuArchitecture
- 4-bit data bus
- 4-bit ALU (add/subtract)
- Custom RAM with decoder
- Register file (X and Y)
- MAR (Memory Address Register)
- Program Counter
- Instruction Register
- Microcoded Control ROM
- 7-segment display output
ROM microcode and opcode present in excel file.

control signals(13 bit microcode)=>
bit 12:  PC_OUT (MSB)
bit 11:  MAR_IN
bit 10:  RAM_OUT
bit 9:  IR_IN
bit 8:  IR_OUT
bit 7:  PC_INC
bit 6:  REG_X_IN
bit 5:  REG_X_OUT
bit 4:  REG_Y_IN
bit 3:  ALU_OUT
bit 2: DISPLAY_IN
bit 1: HLT
bit 0: ADD_SUB (LSB)

Opcode	
00	LDI
01	ADD
10	OUT
11	HLT

