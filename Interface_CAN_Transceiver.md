
##### Transmiter + Rceiver == Transceiver

>>>> 120ohms for mirrored signal of echo like two terminators(resistors connected to opposite wire sides)
>>>> 66ohms for PCM and 2.6kohms for ABS, AT and rest of blocks

##### Nodes
Data link layer

>>> DATA FRAME (Complete CAN Frame)
start of frame -> arbitration field -> control -> data -> crc field -> aknow -> end frame -> idle await (see to draw detailed diagram)

>>> see for rest REMOTE FRAME, INTER FRAME, ERROR FRAME, OVERLOAD FRAME


##### ARBITRATION FIELD

CAN BUS:
>> 0 0 0 1 0 0 0 1 0 1 0 1
NODE1:
>> 0 0 0 1 0 0 1 1 1 1 1 1
NODE2:
>> 0 0 0 1 0 0 0 1 0 1 1 1
NODE3:
>> 0 0 0 1 0 0 0 1 0 1 0 1  WINs!!! =)
NODE4:
>> 0 0 0 1 1 1 1 1 1 1 1 1
NODE5:
>> 0 0 0 1 0 1 1 1 1 1 1 1