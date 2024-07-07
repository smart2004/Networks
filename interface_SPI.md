##### SPI
SPI (Serial Perpheral Interface) - series synchronous data transfer standard @ full duplex, created by Motorola for simple&cheap microcontrollers and periphery connection.
SPI also called as four-wire interface.

###### Data transfer lines/wire
>>> Lead wire (Master)
MOSI(Master Output Slave Input) [DO, SDO, DOUT] #Serial data transfer output
MISO(Master Input Slave Output) [DI, SDI, DIN] #Serial data receive input 
SCLK(Synchronous Clock) [DCCLOCK, CLK, SCK] #Syncronous data transfer output
SS(Slave Select) [CS](Chip Select) #Subordinated selection output(microscheme selection).

>>> Slave wire (Slave)
MOSI(Master Output Slave Input) [DI, SDI. DIN] #Series data receive input
MISO(Master Input Slave Output) [DO, SDO, DOUT] #Serial data transfer output
SCLK(Synchronous Clock) [DCLOCK, CLK, SCK] #Synchronous data receive input
SS(Slave Select) [CS](Chip Select) #Subordinated selection input(microscheme selection).

>>> Data transfer[Two devices direct connection]
Master SPI      Slave SPI
SCLK        ->  SCLK
MOSI        ->  MOSI
MISO        <-  MISO
SS          ->  SS

NOTE: SS[CS] need change state from '1'[default] to '0' switch to for device selection for data transfer.
Next step is to alternate Synchronous CLocK.
Next step is while Synchronous CLocK recession Master makes bit of data, and Slave reads the state per front of Synchronous CLock signal which equals near to middle of bit of data(to avoid front/recession).
Last step is the rest data transfer and once all data received Synchronous clock stops and SS[CS] switch to '1'.

>>> Data transfer[from one to several devices]
NOTE: Same approach, and there should be SS0, SS1, SSn channels for device/devices selection for data transfer. Data may be transfered to several devices simultaneously if switch from '1' to '0' states of SS input receiver.

NOTE: any data may be transmitted trhough SPI interface.

NOTE: Independent connection to several receivers should fit to all available devices.

NOTE: Cascade connection to several devices may fit to some devices. Cascade connection will require less wiring while all transferred date should go through all te receivers anyway, even if some receivers not require some data. 

###### Sync Modes
>>> CPOL == Synchronous Signal initial level (if CPOL=0, then syncronizantion line has low level prior data transfer cycle and after data transfer cycle(i.e. first == raising front, last == recessing), otherwise CPOL=1, which is high(it means first == recessing front, last == raising))

>>> CPHA == Syncronous Phase, detects in which sequence is setting and data sampling (if CPHA=0, then on front, syncronization cycle will implements data sample, and then as per recessing data set is going to happen, in case CPHA=1, then data set should implements as per front in synchronization cycle, and sampling implements per recessing).

CPOL: 0 1 0 1
CPHA: 0 0 1 1

NOTE: Usualy manufacturers already set certain value of CPOL and CPHA as per datasheet reference, read carefully.

###### Dignity:
>> Implementation ease
>> Clock frequency limits by subscribers possibilities and line topology
>> Selection ability of parcel free length & content

###### Flaws:
>> Slave device unable to initiate data interchange (there only one Master on the line)
>> No oficial standard (plenty of implementation options)
