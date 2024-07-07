##### Reference model TCP/IP
>> Application
>> Transport
>> Network(Internet)
>> Data Link

##### Data Link
NOTE: TCP/IP need to connect to existance technology wi-fi or Ethernet

hot spot(access point for wi-fi)==for devices connection

Ethernet switch == connected with several devices through wiring

##### Physical(hardware) addressing
>>> MAC (Media Access Control) addresses
    - uses for network nodes didentification through wi-fi and Ethernet
    - regulated via standard IEEE 802
>>> MAC address format
    - Length 6 byte (48 bit)
    - Record form - 6 HEX numbers:
    1C-75-08-D2-49-45 (IEEE format)
    1C:75:08:D2:49:45 (EITF format)

>>> MAC-address using features:
    - every wi-fi & Ethernet network adapter has embedded MAC-address
    - MAC - addresses in network should be unique

##### Network(Internet)
At Internet level the networks merging those build by different  technologies.
Router is uses to combine different networks.
Heavy networks may contain several routers. The task of Internet level is to find operation path.

>>> Internet (global) addressing
- Global network addresses
    - not joined to network technology
    - uses unique PC identification in composite network

- IP-addresses
    - Global addresses in TCP/IP protocols stack (IP-internet protocol)
    - Record format - four decimal numbersfrom 0 till 255: 192.168.1.1

>>> IP-addresses distribution
- IP-addresses should be unique all over the world
- World IP-address distribution:
    - IANA (Internet Assigned Numbers Authority)
    -RIR (Regional Internet Register)

##### Transport
Processes interaction via network

Client[192.168.1.2]
Same Client another browser[192.168.1.2]
to
Server[192.168.1.100]

NOTE: Transport level allow to interact on different processes and not only with different hardware.

>>> Transport level addressing

- Ports
    - Number in 1 to 65535 range
    - Transport level process address
    - Every network application has own port
    - Port numbers does not repeat
- Record format
    - 192.168.1.100:80

Client[192.168.1.2], browser port [50298]
Same Client another browser[192.168.1.2], browser port [50312]
to
Server[192.168.1.100], browser port [80]

##### Application

>>> Application level protocols
- HTTP (Hypertext Transfer Protocol)
    - Hypertext transfer (Web-pages)
- HTTPS (Hypertext Tranfer Protocol Secure)
- DNS (Domain Name System)
    - Domain name system, IP-address detection through damain name
- SMTP (Simple Mail Transfer Protocol)
    - Email transfer protocol

##### SUMMARY
>>> Network equipment
    - Network interfaces level:
        -wi-fi hot spot, -Ethernet switch
    - Internet level: router

>>> Addressing:
    - Network interfaces level:
        -MAC-addresses
    Internet level:     
        -IP-addresses
    Transport level:
        -Ports
        