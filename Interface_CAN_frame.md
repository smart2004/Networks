##### Complete CAN frame

0 Start of frame

>>> Arbitration Field
0 ID10          
0 ID9 
0 ID8
0 ID7
0 ID6
0 ID5
1 ID4
0 ID3
1 ID2
0 ID1
0 ID0

>>> Data Frame - RTR = 0 / Remote frame - RTR = 0
0 Requ remote

>>> Control
0 ID Ext Bit [Standart frame (11 bit ID) - IDE = 0 / Extended frame (29 bit ID) - IDE = 1]
0 Reserved
0 DL3 [00000000] to detect ahead bits qty
0 DL2 [11110000] to detect ahead bits qty
0 DL1 [11001100] to detect ahead bits qty
1 DL0 [10101010] to detect ahead bits qty

>>> Data Field
0 DB7  Data: 1 to 8 bytes/8 to 64 bits
0 DB6  Data: 1 to 8 bytes/8 to 64 bits
0 DB5  Data: 1 to 8 bytes/8 to 64 bits
0 DB4  Data: 1 to 8 bytes/8 to 64 bits
0 DB3  Data: 1 to 8 bytes/8 to 64 bits
0 DB2  Data: 1 to 8 bytes/8 to 64 bits
0 DB1  Data: 1 to 8 bytes/8 to 64 bits
1 DB0  Data: 1 to 8 bytes/8 to 64 bits

>>> CRC Field - Cyclic redundance check
0 CRC14  Calculated ref to prev fileds
1 CRC13  Calculated ref to prev fileds
0 CRC12  Calculated ref to prev fileds
0 CRC11  Calculated ref to prev fileds
0 CRC10  Calculated ref to prev fileds
0 CRC9   Calculated ref to prev fileds
1 CRC8   Calculated ref to prev fileds
1 CRC7   Calculated ref to prev fileds
0 CRC6   Calculated ref to prev fileds
0 CRC5   Calculated ref to prev fileds
0 CRC4   Calculated ref to prev fileds
0 CRC3   Calculated ref to prev fileds
0 CRC2   Calculated ref to prev fileds
0 CRC1   Calculated ref to prev fileds
0 CRC0   Calculated ref to prev fileds
NOTE: Transmitter node CRC sum CRC Tx should be == to Reciever node CRC sum CRC Rx, in this case data will successfully data transfer without errors, otherwise if not, detected data transfer data error and recieved data going to be ignored
0 CRC Delimeter

>>> Aknow Slot Bit
0  
NOTE: Tx sets '1' recessive state, while Rx sets '0' dominant state that wins of data confirmation and get frame

>>> Aknow Delimiter
1

>>> End of Frame
1 EOF6  Frame finalizing
1 EOF5  Frame finalizing
1 EOF4  Frame finalizing
1 EOF3  Frame finalizing
1 EOF2  Frame finalizing
1 EOF1  Frame finalizing
1 EOF0  Frame finalizing

>>> Idle values
1 IFS2
1 IFS1
1 IFS0

Remote Frame / Inter Frame / Error Frame / Overload Frame
