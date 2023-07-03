# Mosaic-T TimeCard

---
## GNSS Configuration
### Clock reference
The Mosaic-T can be used by an internal or external clock.
The internal clock is a provided by the Mosaic TXCO.
The external clock is the SiT5358 by SiTime.

#### Configuration
To use the internal reference provided by the Mosaic-T a 0 Omh resistor needs to be placed at R3 and R2.
The resistors at R4 and R5 need to be removed.

In turn when using the external reference the R2 and R3 resistors need to be removed and a 0 Omh resistor placed at R4 and R5.

---
### Software
#### Connect to the receiver
**Via USB**
The Windows USB driver provided with your receiver emulates two virtual serial ports, which
can be used as standard COM ports to access the receiver. 
Most terminal emulation programs will make no distinction between virtual and
native COM ports. Note that the port settings (baud rate, etc) for virtual serial ports are not
relevant, and can be left in their default configuration in the terminal emulation program.

##### Windows
When connecting to a Windows computer through USB, a new drive appears in the file manager.
This drive contains an installer for the USB driver. Running this installer is not needed if
you have already installed the RxTools suite.

##### Linux
When connecting to a linux computer no USB drivers need to be installed manually. 
The standard CDC-ACM is suitable.

#### Ethernet over USB
When an USB cable is connected, the receiver supports Ethernet-over-USB. The IP address
allocated to the Ethernet-over-USB interface is 192.168.3.1. That address cannot be
changed, so that this feature is only to be used when a single receiver is connected to your
computer.
