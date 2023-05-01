# add3

## states

new state after 0001 -> 1100
new state after 1100 -> 1101
new state after 1101 -> 0111

## instruction format

op code = 001010

001001 00000 00000 00000 000000 00000
op          rs        rt          rd       ------        rx

## add3.hex

//Load in $8 the number stored at 0x10
8C080010

//Load in $9 the number stored at 0x14
8C090014

//Load in $10 the number stored at 0x18
8C0A0018

//Add \$8, \$9, \$10 and store the result in \$11
2509580A
