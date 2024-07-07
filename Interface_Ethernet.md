#### Ethernet

NOTE: Robert Metcalf from Xerox invented net on split cable: 'The Ether Network' and 'A Cable-Tree Ether'
 
NOTE: Xerox, DEC and Intel agreed to use Ethernet as standard net solution (Ethernet II)

NOTE: In 1982 created IEEE 802.3 project for Etherned standartization, and by end of 1990th Ethernet bacame as dominant technology in local networks

##### OSI Model (place in model)
###### Not active levels for Ethernet
>> Application
>> Presentation
>> Session
>> Transport
>> Network

###### Active levels for Ethernet 
>> Data Link
NOTE: Includes both == Logic channel control sub-level (Logic Link Control, LLC) and Environmental access control (Media Access Control, MAC)
>> Physical

##### Ethernet Types
>> Ethernet, speed: 10Mbit/s [cable: 'thick', 'thin' coaxial, twisted pair, optic] (standard: 802.3)
>> Fast Ethernet, speed: 100Mbit/s [cable: twisted pair, optic] (standard: 802.3u)
>> Gigabit Ethernet, speed: 1Gbit/s [cable: twisted pair, optic] (standard: 802.3z, 802.3ab)
>> 5G Ethernet, speed: 2.5Gbit/s or 5Gbit/s [cable: twisted pair (only)] (802.3bz)
>> 10G Ethernet, speed: 10Gbit/s [cable: twisted pair, optic] (802.3ae, 802.3an)
>> 100G Ethernet, speed: 40Gbit/s or 100Gbit/s [cable: 100Gbit/s, optic] (802.3ba)

NOTE: 10G and 100G Ethernet suitable for servers
NOTE: 5G fits for local networks

##### 2 Ethernet Technologies
###### Classic Ethernet
>>> Shared Environment
>>> Ethernet - Gigabit Ethernet

###### Dial-Up Ethernet
>>> Point-point
>>> Appeared in Fast Ethernet
>>> Only an option in 10G Ethernet and higher

##### Ethernet History

>>> 1st Commmon wire == coaxial cable
PCs connected to coaxial cable with T-connectors
NOTE: in case of fault all network faulted

>>> Hub == device for Ethernet networks creation based on twisted pair (Physical topology == star, Logic topology == common wire)
NOTE: in case of fault, just affected device came became faulted

>>> Ethernet Physical Level
(Coaxial cable, twisted pair, optic)

>>> Data Link
Access and protocols methods, same for any data transfer environment
In classic Ethernet sub-levels LLC and MAC are mixed

###### Frames formats in Ethernet
Standards:
>>> First option == Ethernet to Xerox experimantal implementation
>>> Ethernett II (Ethernet DIX) == Ethernet firm standard of DEC, Intel, Xerox companies
>>> IEEE 802.3 == Ethernet legal standard

NOTE: Standards Ethernet II & IEEE 802.3 slightly differ from each other, Ethernet II uses more frequently, wiil review Ethernet II standard

###### Etherne Frame format
>> Header:
6 bytes 
recipent address

6 bytes
sender address

2 bytes
type
---------------
46...1500 bytes
Data
---------------
>> End switch
4 bytes
check sum

NOTE: Type protpcpl contains protocol code as '0800' == 'IPv4', '86DD' == 'IPv6' or '0806' == 'ARP'

NOTE: In case check sum of sender is equal to check sum of recipent then data going to be accepted otherwise not

NOTE: In case check sum of sender is not equal to check sum of recipent the recipent reject the frame and not inform about this to sender

###### Data field
Contains data of higher level protocol
Max length == 1500 byte
- Selected by Ethernet developers
- Buffer memory size limit
- JumboFrame may applied (which expands the data to 9000 byte)
Min length == 46 bytes
- Ethernet technology limit

###### Ethernet Summary
Ethernet == dominant actual wiring network technology

>> Ethernet technology options:
    - Classic Ethernet
    - Dial-up Ethernet

>> Ethernet technology developmetn
    - Ethernet (10Mbit/s), Fast Ethernet (100Mbit/s), Gigabit Ethernet, 5G Ethernet, 10G Ethernet, 100G Ethernet

Frame format (common for both classic Ethernet and dial-up Ethernet)
