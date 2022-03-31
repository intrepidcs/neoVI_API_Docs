# Unix-like Operating Systems - Support

Support for ValueCAN and neoVI Blue has been added to the ftdi\_sio kernel module in Linux 2.4 and 2.6. Simply load this module and connect either device via USB.

Support for ValueCAN has also been added to the FTDI driver in FreeBSD. neoVI Blue has not been tested at this time, but ought to work.

The current examples available are:

* [`can_sniff`](https://cdn.intrepidcs.net/guides/neoVIDLL/\_downloads/9644d272c28dac0f8b66a6ba3d9e03c4/can\_sniff-0.3.tar.bz2), a command-line tool for monitoring HSCAN traffic.

> can\_sniff includes a library, libintrepidcs, for interfacing with the neoVI and ValueCAN. UNDOCUMENTED FEATURE: can\_sniff supports transmitting messages using this commandline option: -0 “CAN ID: d1 \[d2 … d8]”. For example, to send the message “11 22 33 44” with ID 230, you would run: can\_sniff -0 “230: 11 22 33 44”

* [`can_bitrate`](https://cdn.intrepidcs.net/guides/neoVIDLL/\_downloads/537a961e059d5f8b0eced328fca1c295/can\_bitrate-0.2.tar.bz2), a command-line tool for setting the CNF registers on the neoVI and ValueCAN.
* [`IThinkICAN`](https://cdn.intrepidcs.net/guides/neoVIDLL/\_downloads/9088f6fc61fd96fd00078f5d7c1e8aee/ithinkican-0.4.tar.bz2), the GUI tool for receiving and sending CAN messages on all of HSCAN, SWCAN, MSCAN, and LSFTCAN.

> IThinkICAN requires GTK+-2.4 or later.

The archives are in Bzip2 format - WinRAR is be able to extract them.
