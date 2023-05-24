This board provides support for up to 4 K-type temperature probes as
well as fan PWM support and a USB to serial interface to enhance the
T-962 reflow oven. This also incorporates support for pulse-width modulating
the fan and providing a USB to serial interface for programming.

The firmware source code can be found at
https://github.com/UnifiedEngineering/T-962-improvements

Instructions on how to flash the firmware can be found at
https://github.com/UnifiedEngineering/T-962-improvements/wiki/Flashing-the-LPC21xx-controller

All of the improvements are described on
https://hackaday.com/2014/11/27/improving-the-t-962-reflow-oven/

Note that RXD0 pin on this board must be connected to the TX pin on the T-962
controller and that the TXD0 pin must be connected to the RX pin on the T-962.

If you do not wish for the USB support, do not install the following components:
C6, C9, C10, D1-D3, J8, J10, R3-R9, U7

If you do not need the UART indicators do not install D2, D3, R8 or R9.

If you only want the two internal temperature sensors, do not install
C8, C11, C12, C13, U4 or U6 and replace J2 with a 4 terminal version of the
connector.

If external buttons are added for programming, they can be connected to J9 and
switches SW1 and SW2 do not need to be installed.

Use either the USB-C or J10 for connecting USB.

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
3: RX
4: TX
5: GND

Hook up either J8 or J10, not both

J8: USB-C

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
1   C6,C9 4.7uF X7R 0603
1   D1: ST Microelectronics USBLC6-2SC6
1   D2: Würth Elektronik Red 0603 LED 150060RS75000
1   D3: Würth Elektronik Green 0603 LED 150060VS75020
1   J2: TE 282834-8
1   J3, J5, J6: JST XH-B02B-XH-AM
1   J8: GTC USB4105-GF-A-060 USB-C connector
1   Q1: Infineon BSS214NWH6327XTSA1
1   R1: 4.7K 0603
1   R2: 100K 0603
1   R3: 1K 0603
1   R4: 24K 0603
1   R5: 47.5K 0603
2   R6,R7: 5.1K 0603
2   R8,R9: 560 0603
2   S1, S2: C&K KMR221GLFS LFS
4   U1, U3, U4, U6: Maxim MAX31850KATB+
1   U2: ST Microelectronics LD1117S33CTR
1   U5: Silicon Labs CP2104-F03-GM

All parts can be found at Digikey. The BOM provides both the manufacturer and
Digikey part numbers as well as links to all of the parts on Digikey.  Feel
free to substitute any of the resistors but use 5% or better or any of the
capacitors (use X7R temperature coefficient and make sure the voltages are
appropriate).  There are several variations of the KMR2 C&K buttons, the only
difference is the force required and current.  Any KMR2 button can be used.

Similarly, feel free to substitute LEDs, but the rated voltage should be
2V or lower. If a 3V LED is used you may need to reduce the resistors from
560 owhms to 100 ohms.

The fan mosfet is rated for 1.5A.

The board is designed with Oshpark.com in mind for manufacturing, but most
decent board houses should be able to make these without any difficulty.
