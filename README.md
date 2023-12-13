High Voltage Isolated Measurement Board
===========================================


Introduction
------------
This repository contains hardware files for constructing an isolated high voltage interface board, that output 4mV per volt, allowing measurements up to the kilovolt range (the range can be modified by changing some resistor values).

Specifications (currently untested)
-----------------------------------

HV Input: Up to +-550V (1100V p-p in bipolar mode) or 0-1200V (unipolar mode). The mode is set using two resistors (see the notes in the circuit diagram)

Input Load: 1uA

Frequency Response: DC to 125 kHz

Output: 4mV per Volt

Power Source: 5V DC


Circuit Diagram
---------------
[Click here for PDF schematic](https://github.com/shabaz123/hv_isol_meas/blob/main/hv-isol-meas-schematic-rev1.pdf)
<img width="100%" align="left" src="doc\sch-rev1.png">

Bill of Materials
-----------------

[Click here for PDF BoM](https://github.com/shabaz123/hv_isol_meas/blob/main/hv-isol-meas-bom-rev1.pdf)

The order codes in the last column are Farnell order codes.

| Item | Qty | Reference(s)                           | Value          | Description                                                    | MPN                    | Order Code           |
|------|-----|----------------------------------------|----------------|----------------------------------------------------------------|------------------------|----------------------|
| 1    | 10   | C1, C2, C3, C5, C6, C13, C16, C17, C18, C20 | 1u             | Cap 0805                                                       | GENERIC                | 3369302              |
| 2    | 4   | C4, C9, C14, C15                       | 10u            | Cap 1206                                                       | GENERIC                | 2113073              |
| 3    | 2   | C7, C8                                 | 10p            | Cap 0805 NP0                                                   | GENERIC                | 3369276              |
| 4    | 3   | C10, C11, C12                          | 47u            | Cap Elec 6.3mm dia                                             | GENERIC                | 1144626              |
| 5    | 1   | C19                                    | 100n           | Cap 0805                                                       | GENERIC                | 4061699              |
| 6    | 1   | D3                                     | LED            | LED 1210 Example: ASMT-BG20-AS000                              | ASMT-BG20-AS000        | 1603886              |
| 7    | 1   | J1                                     | SMA Conn       | SMA Right Angle e.g. Molex 73391-0080                          | GENERIC                | 2579835              |
| 8    | 1   | J2                                     | 2-way Pin Hdr  | 2.54mm Pin Header 2-way                                        | GENERIC                | N/A                  |
| 9    | 1   | J3                                     | DC Socket      | DC Socket 5.5+2.1mm, DC10A                                     | FC68148                | 224959               |
| 10   | 3   | L1, L2, L3                             | 2mH            | CM Choke 9.2x6mm Example: SRF0905A-202Y                        | SRF0905A-202Y          | 4203907              |
| 11   | 2   | L4, L5                                 | 200uH          | CM Choke 1210 Example: DLW32MH201XK2L                          | DLW32MH201XK2L         | 2913625              |
| 12   | 1   | OPTO1                                  | HCNR200-300E   | Linear Optocoupler SMD                                         | HCNR200-300E           | 8549710              |
| 13   | 3   | R1, R4                                 | 47k            | Res 0805                                                       | GENERIC                | 9237836              |
| 14   | 1   | R3                                     | 300R           | Res 0805                                                       | GENERIC                | 4177753              |
| 15   | 5   | R5, R8, R9, R13, R16                   | 1k             | Res 0805                                                       | GENERIC                | 1469847              |
| 16   | 1   | R6                                     | 100k           | Res 0805                                                       | GENERIC                | 1469860              |
| 17   | 1   | R11                                    | 39k            | Res 0805                                                       | GENERIC                | 1576482              |
| 18   | 2   | R14, R15                               | 82k            | Res 0805                                                       | GENERIC                | 2447729              |
| 19   | 2   | R7, R17                                | 0R             | Res 2512 0-ohm Example: RC2512JK-070RL                         | RC2512JK-070RL         | 9235825              |
| 20   | 2   | R10, R12                               | 500M           | Res 2512 Vishay CRHP2512AF500MFKE1                             | CRHP2512AF500MFKE1     | 3357767              |
| 21   | 1   | U1                                     | OPA2197DGK     | OpAmp Dual, VSSOP (DGK) package                                | OPA2192 or OPA2197 DGK | OPA2197 is   3117396 |
| 22   | 2   | U2, U5                                 | MCP1541T       | Voltage Ref 4.096V SOT23                                       | MCP1541T-I/TT          | 1084310              |
| 23   | 1   | U3                                     | OPA197         | OpAmp SOT23-5 OPA197IDBVT                                      | OPA197IDBVT            | 3004840              |
| 24   | 1   | U4                                     | 5V DC-DC Isol. | DC-DC 5Vin, +-5Vout Traco TMA, TBA, TMR 2, XP IAxxxxS, IHxxxxS | TMA 0505D              | 1007514              |
| 25   | 1   | U6                                     | TPS60403       | Voltage Inverter Charge Pump SOT23-5                           | TPS60403DBV            | 3123050              |
| 26   | 1   | R18                                    | 47R            | Res 0805                                                       | GENERIC                | 1653007              |
| 27   | 1   | R2                                     | 0R             | Res 0805 0-ohm                                                 | GENERIC                | 1653007              |


Board Layout
-----------------
Top Side:
Note: Capacitor C20 is missing on the Rev 1.0 board. Refer to the Issues list further below, to see where to solder it.
<img width="100%" align="left" src="doc\hvrev1-topside.png">

Underside:
<img width="100%" align="left" src="doc\hvrev1-underside.png">

3D Render
---------
Top Side:
<img width="100%" align="left" src="doc\3drendertop.png">

Underside:
<img width="100%" align="left" src="doc\3drenderunderside.png">

Enclosure
---------
Optionally, the board can be fitted into the following enclosure:
<img width="100%" align="left" src="doc\enclosure.jpg">


PCB CAM Files (Gerber Files)
----------------------------
[Click here for Gerber zip file](https://github.com/shabaz123/hv_isol_meas/blob/main/hv-isol-meas-gerbers-rev1.zip) that can be sent to any PCB factory.

KiCad Source Files
------------------
Download the entire repo and the KiCad 7 files will be in the kicad_src subdirectory.

Issues
------
1. C20 (1uF) is missing from the rev 1.0 board. The photo here shows where to solder it. One end of the capacitor is soldered to the choke L5, and the other end needs to be connected to 0V. The easiest way to access 0V is to scratch off some of the solder mask on the copper pour, and then solder the capacitor to it.
<img width="100%" align="left" src="doc\c20-fix-photo.jpg">
<img width="100%" align="left" src="doc\c20-fix-sch.jpg">

2. The linear optocoupler (OPTO1) footprint is too narrow on the rev 1.0 board : ( The only fix is to use small pliers to bend the SMD optocoupler legs inwards instead of outwards, and then push the vertical parts of the legs inwards too.
<img width="100%" align="left" src="doc\opto-fix-photo.jpg">

3. There is a signal (about 72 kHz) on the output connection : ( It is about 40 mV p-p. I think it's coming from the DC-DC converter. No solution currently for the rev 1.0 board, it is still being worked on.
4. There is an offset on the output, my board had 20 mV offset. Although this could be nulled out on the connected equipment, it will be good to provide an on-board trimmer for nulling. This is still to be worked on.
