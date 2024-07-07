>>> NOTE: simplified many tangled sub-systems with sensors, to have one wire between ECU & sensors
>>> CAN 2.0 A - 11-bit
>>> CAN 2.0 B - 29-bit
>>> CAN FD 8Mbit/sec

ISO 11898-1 CAN Data link layer
ISO 11898-2 CAN HS physical layer
ISO 11898-3 CAN LS physical layer

CAN based on two layers (Physical & Data Link) ref _OSI file for other layers
NOTE: CAN is a close network == no need for security, sessions or logins, no user interface requirements

##### HI SPEED CAN (ISO 11898-2) - 1Mbit/s(actual 500kbit/s)
>>> CAN HI = CAN LOW = 2.5V [CAN HI - CAN LOW = 0V == '1' RECESSIVE]
>>> CAN HI = 3.5V, CAN LOW = 1.5V [CAN HI - CAN LOW = 2V == '0' DOMINANT]

##### LOW SPEED CAN (ISO 11898-3) - up to 125kbit/s [can operate in one wire mode if second broken]
>>> CAN HI = 0V, CAN LOW = 5V [CAN LOW - CAN HI = 5V == '1' RECESSIVE]
>>> CAN HI = 3.6V, CAN LOW = 1.4V [CAN HI - CAN LOW = 2.2V == '0' DOMINANT]

NOTE: DOMINANT '0' WINS RESCESSIVE '1'

MAIN engine blocks: ECM ICM L-Jetronic KE-Jetronic Motronic Digifant Mono-Motronic 
MAIN transmission: TCM PCM 
MAIN brake system: ABS BAS ESP DSC VSC
AUX blocks(climatew control, enjoy blocks, etc.): HVAC IC BCM BSI SRS SAM MMI CEM

WWH-OBD [World-Wide Harmonized On-Board Diagnostics]