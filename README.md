# Github-Tutorial
Hey, this is for tutorial purposes!

The key takeway here is that when porting Ben's programs you have to use this "mapping table":
|Segment|BE6502 |DB6502 |Comment |
|-------|-------------|-------------|------------------------------------------------------------------|
|RAM |0x0000-0x3fff|0x0000-0x7fff| |
|VIA1 | |0x9000 |Connected to keyboard/LCD/blink LED in my build |
|VIA2 |0x6000 |0x8800 |Can be used to run Ben's programs |
|ACIA | |0x8400 | |
|ROM |0x8000-0xffff|0xa000-0xffff|**First 8K are not accessible, but need to be burned to the chip**|
