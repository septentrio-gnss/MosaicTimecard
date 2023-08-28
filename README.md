# Mosaic-Timecard

<!-- 

- AIM+
- IONO+
- Accuracy with AtomiChron
- Multi-constellations, multi-band
- Purpose of Timecard & RCB
- Connectors on the board

-->

---
## What is the Time Card
The Time Card is the heart of the [Open Time Server](https://github.com/opencomputeproject/Time-Appliance-Project/tree/master/Open-Time-Server/) project.

Accurate timing is a critical part of a PTP enabled network. 
The Time Card provides this via GNSS while maintaining accuracy in case of GNSS signal loss or failure by using a high stability and holdover oscillator.
The Time Card project was created to provide a open source solution via a PCIe card.

## How the Time Card is used
The Timecard can generally be used in 2 ways: Standalone and in a Full System.
In using the Timecard as standalone, you only need the Timecard and a device
with PCIe capabilities. 
You now have the option to retrieve a PHC (Physical Hwardware Clock) time which can be set for system time.
This is done over PCIe where the Timecard shows up as a device.
For PPS output this is available over the U.FL connectors on the Timecard and can be used as needed.
 
The other way is to integrate the Timecard into a full system.
This includes a NIC (Network Interface Card) and the Timebeat software.
The way this system works is the Timecard is plugged into a PCIe slot.
Which powers the board and starts providing PPS output over U.FL connectors.
These can be plugged into a NIC with a U.FL adapter. 
This then provides the NIC with PPS from the Timecard. 
The software running on the device takes this input and converts it onto PTP (Precision Time Protocol). 
Which in turn can be used to synchronise devices on the network.

## Purpose of the Mosaic RCB
The Mosaic-T available on the M.2 (RCB) receiver carrier board provides PPS
output coming from GNSS satellites. 
The route of this PPS signal originates from the Mosaic-T, then goes into the FPGA which does some filtering and correction.
This in turn becomes an input for the oscillator. 
The main use for the GNSS receiver is to control the drift from the oscillator. 
If the GNSS receiver loses signal the oscillator still provides accurate PPS until the receiver can regain signal.
Once the PPS signal has passed through the oscillator this signal is exposed using U.FL
connectors on the Timecard.

---
### How to produce the Time Card and Mosaic RCB
[Production](Production.md)  

### How to configure the Time Card and Mosaic
[configuration](Configuration.md)  

### How to use the Time Card
[Application](Application.md)
