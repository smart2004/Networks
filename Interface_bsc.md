Interface - mode and method set of two or more systems interaction, hardware or soft information exchange between each other, define per specification, connections specification, signals exchange etc.

##### Interface classification

#### Iformation exchange
>>> parallel
>>> series
>>> series-parallel

#### Data transfer mode
>>> Synchronous
>>> Asynchronous

#### Information exchange mode
>>> Duplex
>>> Simplex
>>> Semi-Duplex
>>> Multiplex

#### Parallel interface
Transmitter (TX)                Reciever (RX)
D7                  0 (MSB)     D7
D6                  1           D6
D5                  1           D5
D4                  0           D4
D3                  0           D3
D2                  0           D2
D1                  1           D1
D0                  1 (LSB)     D0          

#### Series interface
Transmitter (TX) Dout              Receiver (RX) Din
D0(LSB[1]) D1[1] D2[0] D3[0] D4[0] D5[1] D6[1] D7[0]

NOTE: Some SPI microcheme may have frequency 18MHz
NOTE: Speed increase lasts for many difficulties (long distance, equal wires etc)

>>> Synchronous == data transfer along with tact signal (example I2C, SPI)
>>> Asynchronous == data transfer does not lasts with tact signal (example USB, Ethernet)

#### Information data exchange
>>> Duplex == data trasfer may be simultaneously to both ends @ any time
>>> Simplex == data transfer may be to one end (only)
>>> Semiduplex == transfer may be done by any end if interface is free
>>> Multiplex == data exchange may be done between any modules pair

#### Index
>>> Transmitter == element one transmit data to bus
>>> Receiver == element one receive data from bus
>>> Slave == element addressed by master
>>> Multi-master == System that has more than one master
>>> Arbitrage == guaranteed procedure in case more than one master simultaneously attempting to control the bus, one of it only will grant full access for bus control and provide data transfer without errors

NOTE: I2C may have one master and several slaves
