This board provides support for up to 4 K-type temperature probes as
well as fan PWM support and a USB to serial interface to enhance the
T-962 reflow oven.

Connectors:

J1: Connect to T962 controller board
1: DQ
2: FAN_PWM
3: GND

J2: Thermocouple connector
1: T3+
2: T3-
3: T2+
4: T2-
5: T1+
6: T1-
7: T0+
8: T0-

J3: 12V in
1: GND
2: +12V

J4: +3V out
1: GND
2: +3V

J5: Fan out
1: PWM (GND)
2: +12V

J6: +12V out
1: GND
2: +12V

J7: Programming Header, connect to T962 controller board header
1: N_ISP
2: N_RST
3: TX
4: RX
5: GND

Hook up either J8 or J10, not both

J8: Micro USB

J9: N_ISP and N_RST for external buttons
1: N_RST
2: GND
3: N_ISP

J10: USB
1: GND
2: D+
3: D-
4: +5V


BOM:
QTY Ref
5   C1,C4,C8,C10,C12: 0.1uf X7R 0603
4   C2,C5,C11,C13 0.01uF X7R 0603
1   C3 1uF X7R 0603
1   C9 4.7uF X7R 0603
1   D1: ST Microelectronics USBLC6-2SC6
1   J2: TE 282834-8
1   J3, J5, J6: JST XH-B02B-XH-AM
1   J8: Molex 105017-0001
1   Q1: Infineon BSS214NWH6327XTSA1
1   R1: 4.7K 0603
1   R2: 100K 0603
1   R3: 1K 0603
1   R4: 22.1K 0603
1   R5: 47.5K 0603
2   S1, S2: C&K KMR231NG LFS
4   U1, U3, U4, U6: Maxim MAX31850KATB+
1   U2: ST Microelectronics LD1117S33CTR
1   U5: Silicon Labs CP2102N-A01-QFN24

All parts can be found at Digikey, however the MAX31850KATB+ is considerably
less expensive at Mouser.
