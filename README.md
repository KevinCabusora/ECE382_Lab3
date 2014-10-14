ECE382_Lab3
===========
Kyle Jonas
M6 Dr Coulston
Lab3 SPI - "I/O"


##Mega-Prelab

####Nokia 1202 LCD BoosterPack v4-5

MS430 Family Guide p328-329

####Configure the MSP430 

MSP430 p328-329

MSP430 Family Guide p445

####Configure the Nokia 1202 Display

STE2007 p41


##Lab

####Logic Analyzer

| Line | R12    | R13    | Purpose                                                                                                    |
|------|--------|--------|------------------------------------------------------------------------------------------------------------|
| 66   | `0x01` | `0xE7` | R12 Parameter to writeNokiaByte specifying data, R13 Holds the data for the 8-bit vertical bar `1110 0111` |
| 276  | `0x00` | `0xB0` | R12 specifies command, R13 sets page (aka row) address to `0xB0`                                           |
| 288  | `0x00` | `0x10` | R12 specifies command, R13 `0x10` is the prefix for upper 4-bits in the column                             |
| 294  | `0x00` | `0x00` | R12 specifies command, R13`0x00` is the prefix for lower 4-bits in the column                               |

####Waveforms

| Line | Command/Data | 8-bit Packet |
|------|--------------|--------------|
| 66   | Data         | 1110 0111    |
| 276  | Command      | 1011 0010    |
| 288  | Command      | 0001 0000    |
| 294  | Command      | 0000 0100    |

Line 66
![Line 66](https://github.com/KyleJonas/ECE382_Lab3/blob/master/Pictures/Line%2066.png?raw=true "Line 66")

Line 276
![Line 276](https://github.com/KyleJonas/ECE382_Lab3/blob/master/Pictures/Line%20276.png?raw=true "Line 276")

Line 288
![Line 288](https://github.com/KyleJonas/ECE382_Lab3/blob/master/Pictures/Line%20288.png?raw=true "Line 288")

Line 294
![Line 294](https://github.com/KyleJonas/ECE382_Lab3/blob/master/Pictures/Line%20294.png?raw=true "Line 294")
