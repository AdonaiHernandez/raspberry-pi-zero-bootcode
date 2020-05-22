# raspberry-pi-zero-bootcode
El bootcode.bin lo unico que hace es parpadear el led de actividad en la placa

# Hex dump
0x000  || 00                  ;Pading de 200 bytes
0x200  || 01 E8 10 00 20 7E   ;mov r1, 0x7e200010
0x206  || 10 08               ;ld r0, r1
0x208  || E0 E8 FF FF 1F FF   ;and r0, 0xff1fffff
0x20E  || A0 E9 00 00 20 00   ;or r0, 0x00200000
0x214  || 10 09               ;st r0, r1
0x216  || 01 E8 20 00 20 7E   ;mov r1, 0x7e200020
0x21C  || 02 E8 20 00 20 7E   ;mov r2, 0x7e200020
0x222  || 03 E8 00 80 13 09   
0x228  || 00 60
0x22A  || 10 62 
