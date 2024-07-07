##### RS-232
>>> Series asyncronous binary data transfer between terminal and communication device
>> 1 pin [DCD]
>> 2 pin [RxD]
>> 3 pin [TxD]
>> 4 pin [DTR]
>> 5 pin [GND]
>> 6 pin [DSR]
>> 7 pin [RTS]
>> 8 pin [CTS]
>> 9 pin [RI]

>>> Max device qty: 2
>>> Max distance: 15m
>>> Max data transfer: up to 115299 bod
>>> Lines voltage: -15V...+15V
>>> Log "1" level: -3V...-15V
>>> Log "0" level: +3V...+15V

###### Baud
>>> Symbol speed measurement unit, inform parameter recurrent carrier signal variation quantity /per second

>> In RS-232/UART usually requre 10 bit for 1 byte transfer, therefore 1 bod == 0.8 bit/second

>> Another example: @ quadrature modulation of 16-QAM 1 bod = 16 bit/sec

###### Time diagram
>>>NOTE: if initially data does not transfer to any side we have log "1" on line

NOTE: Transmitter and Receiver shoud be set to one ssame speed. for example 9600baud/s(bps)

                Transmitter Receiver
start bit[0]    0           0.5t        
1[0/1]          t           1.5t
2[0/1]          2t          2.5t
3[0/1]          3t          3.5t
4[0/1]          4t          4.5t
5[0/1]          5t          5.5t
6[0/1]          6t          6.5t
7[0/1]          7t          7.5t
8[0/1]          8t          8.5t
P(parity)[0/1]  9t          9.5t
stop bit1[1]    10t         10.5t
stop bit2[1]    11t         11.5t
expectation[1]  12t         -
                0           0

NOTE: Parity bit == control additional bit, serves for binary parity overall check (singular bits parity in number). Parity bit calculates within 'exception OR' operation.
As example: 10111101 contains 6 '1'bits, parity bit == 0
            01110011 contains 5 '1'bits, parity bit == 1
            00000000 contains 0 '1'bits, parity bit == 0
