# swap

## states

new state after 0001 -> 1100

new state after 1100 ->1101

## instruction format

- op 001001

- rs

- rt

- rd

- unused

rs == rd

## swap.hex

load in \$8 the number in memory at 0xC 

load in \$9 the number in memory at 0x10

swap \$8 and \$9
001001 01000 01001 01000 00000000000
