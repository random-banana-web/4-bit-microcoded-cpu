# 4-bit Microcoded CPU

A 4-bit CPU built from scratch in Logisim Evolution, featuring a 
custom datapath, microcoded control unit, and 7-segment display output.

## Architecture
- 4-bit data bus
- 4-bit ALU (add/subtract)
- Custom RAM with decoder
- Register file (X and Y)
- MAR (Memory Address Register)
- Program Counter
- Instruction Register
- Microcoded Control ROM
- 7-segment display output

## Instruction Set
| Opcode | Instruction | Operation |
|--------|-------------|-----------|
| 00     | LDI         | Load immediate value into Register X |
| 01     | ADD         | Add immediate value to Register X |
| 10     | OUT         | Output Register X to display |
| 11     | HLT         | Halt execution |

## Control Signals (13-bit microcode word)
| Bit | Signal | Description |
|-----|--------|-------------|
| 12  | PC_OUT | Program Counter onto bus |
| 11  | MAR_IN | Load bus into MAR |
| 10  | RAM_OUT | RAM onto bus |
| 9   | IR_IN  | Load bus into IR |
| 8   | IR_OUT | IR operand onto bus |
| 7   | PC_INC | Increment PC |
| 6   | REG_X_IN | Load bus into Register X |
| 5   | REG_X_OUT | Register X onto bus |
| 4   | REG_Y_IN | Load bus into Register Y |
| 3   | ALU_OUT | ALU result onto bus |
| 2   | DISPLAY_IN | Latch bus into display register |
| 1   | HLT | Halt clock |
| 0   | ADD_SUB | ALU mode (0=add, 1=sub) |

## Files
- `4bitCPU.circ` - Logisim Evolution circuit file
- `Micro code cpu.xlsx` - Control ROM microcode table


## Built With
- Logisim Evolution v4.1.0
