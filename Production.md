# Production Mosaic-Timecard

<!-- 

- MosaicHAT  
    https://github.com/septentrio-gnss/mowi#how-to-produce-mowi

-->

---
## Clock reference
### Internal clock
To use the internal clock referenced provided by the Mosaic's TXCO.
The resisters for R2 and R3 need to be jumped with a 0 Ohm resistor.
R4 and R5 should be left empty and floating

### External clock
In turn when using the external clock reference instead of the internal reference.
R2 and R3 should be empty and floating while R4 and R5 should be jumped by a 0 Ohm resistor.
