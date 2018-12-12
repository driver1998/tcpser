# tcpser
This is yet another fork of Jim Brain's tcpser program.

It is mainly used for networking for the Windows on Raspberry project. \
Since we don't have network drivers working on Windows ARM64 on Raspberry Pi, networking over serial is our best bet.

Support for 230400, 460800 and 921600bps is added, to get the fastest speed possible.

Hardware flow control (CRTSCTS) bit is now unmodified during startup. \
Setting that bit causes problems on some hardware, like the CP2102 based USB to TTL adapter. \
If you need hardware flow control (the RTS/CTS pins), simpliy set it manually using `AT&K3` command.
