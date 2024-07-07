##### MAC Addresses
Related to OSI model placed on:
>> Data Link
 NOTE: Includes both == Logic channel control sub-level (Logic Link Control, LLC) and Environmental access control (Media Access Control, MAC)

MAC-addresses serves to network interfaces nodes identification as:
- Ethernet (IEEE 802.3)
- Wi-Fi (IEEE 802.11)

Standartized by IEEE 802:
- Data length 6 bytes (48 bytes)

Record form: 6 HEX numbers:
- 1C-75-08-D2-49-45
- 1C:75:08:D2:49:45

###### MAC Adresses types
>> Private (unicast):
- 30-9C-23-15-E8-8C

>> Group (multicast, dirst bit of senior byte == 1):
- 01-80-C2-00-00-08

>> Broadcast (broadcast, all 1)
- FF-FF-FF-FF-FF-FF

###### MAC Addresses unique
There shouldn't be same MAC-addresses in one network region:
- One Ethernet/Wi-Fi broadcast envoronment 
- One VLAN at dial-up Ethernet
NOTE: In case there would be 2 PCs with same MAC-address, one of it wouldn't work. Which one does nt specified.

###### MAC Addresses Assign
Centralized(by default):
- Addresses assigned by Equipment Manufacturer
- The assign rules described in IEEE 802 standard

Local:
- Addresses assigned by network admin
- Unique should be provided by admin

Assignation method indicator - the second bit of MAC Address senior byte:
- 0 == centralized address assignation
- 1 == local address assignation

###### Assignation approaches
As per centralized MAC addresses assignation should be unified

MAC-addresses structure:
- First three bytes == unique organization identifier (Organizationally Unique Identifier, OUI), IEEE sets by equipent manufacturers
- Last three bytes == assigned by equipment manufacturer

OUI example:
- 00:00:0C == Cisco (or 6C:50:4D and 70:81:51 etc)
- 00:02:B3 == Intel
- 00:04:AC == IBM

###### MAC Address check
Command string:
- Windows == 'ipgonfig /all'
- Linux == 'ifconfig' or 'ip link'

###### Summary
MAC addresses == Data Link
MAC addresses should be unique
MAC addresses usage:
- Ethernet
- Wi-Fi
MAC Addresses assignation:
- Automatic by network adapters manufacturers
- Manual
