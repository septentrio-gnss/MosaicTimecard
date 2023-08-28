# Production Mosaic-Timecard

<!-- 

- MosaicHAT  
    https://github.com/septentrio-gnss/mowi#how-to-produce-mowi

-->

## Time Card production
To produce the Time Card without the GNSS RCB yourself all the necessary code, BOM, Gerber files and binaries are available on the [official github](https://github.com/opencomputeproject/Time-Appliance-Project/tree/master/Time-Card/HW)
Videos are provided by the Open Compute Project which explain the step by step process.
[Order Time Card Baseboard](https://www.youtube.com/watch?v=qPRaQU9TBTw)
[Order Time Card Accessories](https://www.youtube.com/watch?v=4X3i5tge4S4)

The files to produce the Mosaic RCB are found in the [Hardware folder](/Hardware)

## Clock reference
### Internal clock
To use the internal clock referenced provided by the Mosaic's TXCO.
The resisters for R2 and R3 need to be jumped with a 0 Ohm resistor.
R4 and R5 should be left empty and floating

### External clock
In turn when using the external clock reference instead of the internal reference.
R2 and R3 should be empty and floating while R4 and R5 should be jumped by a 0 Ohm resistor.
