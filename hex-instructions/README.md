## Hex files in this folder

- `j.hex`: Jumps to 0x20 (= 0x8<<2).

- `lw.hex`: The number 0xF is stored in memory at 0xC. Load the number stored in 0xC in \$8.

- `sw.hex`: The number 0xF is stored in memory at 0xC. Load the number stored in 0xC in \$8. Store \$8 register in memory at 0x12.

- `add.hex`: The number 0xF is stored in memory at 0xC. The number 0x4 is stored in memory at 0x10. Load the two numbers from memory in \$8 and \$9. Add the two registers and store the result in \$10.

- `beq.hex`: Check if \$8 is equal to \$0. If true jump to PC+4+(0x8<<2).

## Instructions format

LOAD WORD:

op     rs    rt    offset
100011 00000 00000 0000000000000000

Load the 32-bit quantity (word) at address into register rt.

---

STORE WORD:

op     rs    rt    offset
101011 00000 00000 0000000000000000

Store the word from register rt at address.

---

JUMP:

op     target
000010 00000000000000000000000000

Unconditionally jump to the instruction at target.

---

BEQ:

op     rs    rt    label
000100 00000 00000 0000000000000000

Conditionally branch the number of instructions specified by the offset if
register rs equals rt.

---

ADD:

op     rs    rt    rd    zero  funct
000000 00000 00000 00000 00000 100000

Put the sum of registers rs and rt into register rd.

---

AND:

op     rs    rt    rd    zero  funct
000000 00000 00000 00000 00000 100100

Put the logical AND of registers rs and rt into register rd.

---

SUB:

op     rs    rt    rd    zero  funct
000000 00000 00000 00000 00000 100010

---

SLT:
op     rs    rt    rd    zero  funct
000000 00000 00000 00000 00000 101010
