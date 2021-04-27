## ## Hex files in this folder

- `j.hex`: jumps to 0x8 << 2

- `lw.hex`

- `sw.hex`

- `add.hex`

- `beq.hex`







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
