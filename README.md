# Asynchronous Serial Data Splitter

This application demonstrates asynchronous data transfer between serial ports using the ser.notifysent syscall. The idea is to emulate the data flow in a system with one master serial port and multiple slave ports.

Serial port 0 is the master port and ports 1-3 are the slave ports. Data from the master port is sent to all three slave ports and data coming in from any of the slave ports is sent to the master port.

There is also a telnet data dump monitor on port 65535. The following commands are supported:

- **A**: View all ports
- **2**: View Master + COM1
- **3**: View Master + COM2
- **4**: View Master + COM3
- **P**: Pause
- **U**: Switch into firmware upload mode

When the U command is issued, it switches the serial port to firmware upload mode. While in this mode, data coming into that port will no longer be redirected.