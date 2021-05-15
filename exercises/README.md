# Exercises

## addi

Follow the standard addi instruction found in MIPS32.

## jal

Follow the standard addi instruction found in MIPS32.

## jrim

"Jump register immediate". 

jrim imm(\$rs):

- imm is a 16-bit value

- jumps to \$rs + imm

Instruction structure:

- 6 bit OPCODE 111111 [bit 26-31]

- 5 bit \$rs REGISTER FIELD [bit 21-25]

- 16 bit IMMEDIATE [bit 0-15]

- NOT SPECIFIED \$rt [bit 16-20]

## swap

swap \$rs, \$rt: swap the contents of the two registers

## add3

add3 \$rd, \$rs, \$rt, \$rx

\$rd = \$rs + \$rt + \$rx

Instruction structure:

- 6 bit OPCODE xxxxxx [bit 26-31]

- 5 bit \$rs [bit 25-21]

- 5 bit \$rt [bit 20-16]

- 5 bit \$rd [bit 15-11]

- 6 bit NOT USED [bit 10-5]

## overflow exception
2 different implementations of overflow exception
(note: due to the current overflow detection in the ALU this works only for add operations)

## load word not aligned exception
simple implementation for load word with address not aligned in memory

- 5 bit \$rx [bit 4-0]
