##### RS-485/422

>> Max devices number: 32 (up to 256 with special microschemes)
>> Max distance: 1200m
>> Max data transfer speed: up to 10Mbit/s
>> A and B voltge related to GND: -7..+12V
>> Log "1" level: Uab > +200mV
>> Log "0" level: Uab < -200mV

NOTE: Good noise defence, simple realization
NOTE: Awesome for tasks with not too fast data transfer needs

###### Transmitter requirements:
>> +2V...+6V [logic '0']
>> -2V...-6V [logic '1']

###### Receiver requirements:
>> +200mV...+6V [logic '0']
>> -200mV...-6V [logic '1']

NOTE: Absolute max voltage may be +12V/-12V
NOTE: For RS-422 for one line may be just one transmittrer only and several receivers. 
For duplex data transfer need one more twisted pair. 
In case of long line need Rc=120 Ohms wave resistor (terminator).
Because of twisted pair this has strong defence from other noises.

NOTE: for RS-485 for one line may be conducted data transmission and data receive.
On the line at one time period just one transmitter can operates.
In case of long line need Rc=120 Ohms wave resistor (terminator). Terminator here available from both sides.
Because of twisted pair this has strong defence from other noises.

NOTE: Terminators usually equals to 120 Ohms as wave resistance normalized to 120 Ohms.
In case of coaxial cable wave resistance 50 Ohms there should be 50 Ohms terminators.

NOTE: GND of all devices shoud be connected together to have common GND and have standartized voltage refer to any combined devices (GND potencial equalizing). To protect from burn failure.
NOTE: Drain should be connected to one point. Drain connected through resistor to one point.

NOTE: If need transmit data to long distance there should be four wires: A, B, GND and Drain. In case distance is short this topology may be simplified.
