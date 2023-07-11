# Configuration Mosaic-Timecard

<!-- 

- Ethernet over USB
- AtomiChron  
    https://customersupport.septentrio.com/s/article/Activating-Septentrio-receivers-for-AtomiChron
- Kernel build  
    https://opencomputeproject.github.io/Time-Appliance-Project/docs/time-card/installation
- FPGA flashing  
    https://github.com/opencomputeproject/Time-Appliance-Project/tree/master/Time-Card/FPGA/Open-Source

-->

---

## Connect to Mosaic
### Over USB
##### Windows
The Windows USB driver provided with your receiver emulates two virtual serial ports, which
can be used as standard COM ports to access the receiver. 
Most terminal emulation programs will make no distinction between virtual and
native COM ports. Note that the port settings (baud rate, etc) for virtual serial ports are not relevant, and can be left in their default configuration in the terminal emulation program.

When connecting to a Windows computer through USB, a new drive appears in the file manager.
This drive contains an installer for the USB driver. Running this installer is not needed if you have already installed the RxTools suite.

##### Linux
When connecting to a linux computer no USB drivers need to be installed manually. 
The standard CDC-ACM is suitable.

### Ethernet over USB

When an USB cable is connected, the receiver supports Ethernet-over-USB. The IP address
allocated to the Ethernet-over-USB interface is 192.168.3.1. That address cannot be
changed, so that this feature is only to be used when a single receiver is connected to your
computer.