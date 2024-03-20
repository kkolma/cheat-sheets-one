This comprehensive ARM Assembly cheat sheet provides a fundamental overview of [ARM assembly programming](https://developer.arm.com/documentation/107829/0200/Assembly-language-basics), including registers, update modes, and memory addressing, as well as a detailed list of essential ARM instructions such as arithmetic, branching, bitwise logic, comparison, data movement, and memory access operations. It serves as a quick reference for beginners and seasoned programmers alike, offering insights into the basics of ARM architecture and instruction set to facilitate data manipulation, function management, and efficient memory handling.

## The Basics
### Registers (`reg`)

In ARM assembly language, registers are denoted by `reg` and can refer to any of the general-purpose registers or specific system registers. Here is the explanation of the register naming conventions:

- `R0` to `R15`: General-purpose registers, where the number indicates the specific register. These are used for a wide range of purposes, from holding data and addresses to intermediate calculations.
- `SP` (Stack Pointer): This is register `R13`. It is used to point to the last item in the stack, a critical function in managing function calls and local variables.
- `LR` (Link Register): Register `R14` serves as the link register. It typically holds the return address when a subroutine is called, allowing the program to return to the correct location after the subroutine is completed.
- `PC` (Program Counter): Register `R15` acts as the program counter. It holds the address of the next instruction to be executed. Changing the value of `PC` can thus alter the flow of execution in the program.

These registers are integral to ARM assembly programming, facilitating data manipulation, function call management, and control flow.

### Update Mode (`um`)

The update mode (`um`) specifies how the base register is updated during multiple register load/store instructions. The following are the update modes available in ARM assembly:

- `FA` / `IA`: Full Ascending / Increment After - The base register is updated to point to the next address after the current block of data. This mode starts accessing memory at the current base register address and increments the address after each access.
- `EA` / `IB`: Empty Ascending / Increment Before - The base register is updated to point to the next address before accessing the current block of data. This mode increments the base address before accessing memory, starting with the new address.
- `FD` / `DB`: Full Descending / Decrement Before - The base register is updated to point to the previous address before accessing the current block of data. This mode starts by decrementing the base address and then accessing memory starting from this new address.
- `ED` / `DA`: Empty Descending / Decrement After - The base register is updated to point to the previous address after accessing the current block of data. This mode accesses memory starting at the current base register address and decrements the address after each access.

These modes determine how the base register's value is adjusted in relation to the data block being loaded or stored, allowing for efficient memory access patterns, especially in looping constructs or when managing arrays and buffers.

### Memory Address (`mem`)

Memory addressing modes specify the address used for load and store operations. The following are the formats used to specify memory addresses in ARM assembly instructions:
- `[reg #±imm 12]`: Direct offset - The address is the base register (`reg`) offset by a constant (`±imm 12`), where `imm` is a 12-bit immediate value.
- `[reg±reg]`: Register offset - The address is the base register (`reg`) offset by another register value.
- `[rega±regbshift]`: Scaled register offset - The address is the base register (`rega`) offset by a scaled (shifted) register value (`regb`), where `shift` specifies the type and amount of shift applied to `regb`.
- `[reg #±imm 12]!`: Pre-indexed addressing - The base register is updated with the offset address before the memory access.
- `[reg±reg]!`: Pre-indexed register offset - Similar to direct pre-indexed, but the offset is another register.
- `[reg±reg shift ]!`: Pre-indexed scaled register offset - The base register is updated with the scaled (shifted) register offset before the memory access.
- `[reg]#±imm 12`: Post-indexed addressing - The memory access occurs using the base register, which is then updated with the offset.
- `[reg]±reg`: Post-indexed register offset - The memory access uses the base register, which is then updated with another register value.
- `[reg]±regshift`: Post-indexed scaled register offset - The memory access uses the base register, which is then updated with a scaled (shifted) register offset.




## ARM Instructions

### Arithmetic

- `ADDcdS reg reg arg` - add
- `SUBcdS reg reg arg` - subtract
- `RSBcdS reg reg arg` - subtract reversed operands
- `ADCcdS reg reg arg` - add both operands and carry flag
- `SBCcdS reg reg arg` - subtract both operands and adds carry flag − 1
- `RSCcdS reg reg arg` - reverse subtract both operands and adds carry flag − 1
- `MULcdS regd regm regs` - multiply regm and regs places lower 32 bits into regd
- `MLAcdS regd regm regs regn` - places lower 32 bits of regm · regs + regn into regd
- `UMULLcdS reglo reghi regm regs` - multiply regm and regs place 64-bit unsigned result into {reghi reglo}
- `UMLALcdS reglo reghi regm regs` - place unsigned regm · regs + {reghi reglo} into {reghi reglo}
- `SMULLcdS reglo reghi regm regs` - multiply regm and regs place 64-bit signed result into {reghi reglo}
- `SMLALcdS reglo reghi regm regs` - place signed regm · regs + {reghi reglo} into {reghi reglo}

### Branching

- `Bcd imm24` - branch to imm 24 words away
- `BLcd imm24` - copy PC to LR then branch
- `BXcd reg` - copy reg to PC and exchange instruction sets (T flag := reg[0])
- `SWIcd imm24` - software interrupt

### Bitwise Logic

- `ANDcdS reg reg arg` - bitwise AND
- `ORRcdS reg reg arg` - bitwise OR
- `EORcdS reg reg arg` - bitwise exclusive-OR
- `BICcdS reg rega argb` - bitwise rega AND (NOT arg b)

### Comparison

- `CMPcd reg arg` - update flags based on subtraction
- `CMNcd reg arg` - update flags based on addition
- `TSTcd reg arg` - update flags based on bitwise AND
- `TEQcd reg arg` - update flags based on bitwise exclusive-OR

### Data Movement

- `MOVcdS reg arg` - copy argument
- `MVNcdS reg arg` - copy bitwise NOT of argument

### Memory Access

- `LDRcdB reg mem` - loads word/ byte/ half from memory into a register
- `STRcdB reg mem` - stores word/ byte/ half to memory from a register
- `LDMcd um reg! mreg` - loads into multiple registers
- `STMcd um reg! mreg` - stores multiple registers
- `SWPcdB regd regm [regn]` - copies regm to memory at regn, old value at address regn to regd


### Shift
- `LSL #imm 5`: shift left 0 to 31
- `LSR #imm 5`: logical shift right 1 to 32
- `ASR #imm 5`: arithmetic shift right 1 to 32
- `ROR #imm 5`: rotate right 1 to 31
- `RRX`: rotate carry bit into top bit
- `LSL reg`: shift left by register
- `LSR reg`: logical shift right by register
- `ASR reg`: arithmetic shift right by register
- `ROR reg`: rotate right by register

### Notes:

- `S` = set condition flags
- `B` = byte, can be replaced by H for half word(2 bytes)
- `cd`: condition code (e.g., `AL` or omitted for always, `EQ` for equal, `NE` for not equal, etc.)
- `reg`: register (e.g., `R0 to R15`, `SP` for stack pointer, `LR` for link register, `PC` for program counter)
- `arg`: right-hand argument (e.g., `#imm 8` for immediate on 8 bits possibly rotated right, `reg` for register, etc.)
- `shift`: shift register value (e.g., `LSL #imm 5` for shift left 0 to 31, `LSR #imm 5` for logical shift right 1 to 32, etc.)
- `mem`: memory address (e.g., `[reg #±imm 12]` for register offset by constant, `[reg±reg]` for register offset by variable bytes, etc.)
