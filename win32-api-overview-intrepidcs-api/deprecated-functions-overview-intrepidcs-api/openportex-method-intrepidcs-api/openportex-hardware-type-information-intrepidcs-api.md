# OpenPortEx Hardware Type Information - intrepidcs API

This topic discusses which port type can be used with what type of hardware.

A required parameter for the OpenPortEx command is the Port type. Each type is and the hardware it supports is listed below.

| Port type type | Applicable hardware                                                                                                                             | Notes                                                                                                                                             |
| -------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| RS232          | <ul><li>neoVI Blue (USB or RS232 connection)</li><li>neoVI Pro (USB or RS232 connection)</li><li>neoVI Green (RS232)</li><li>ValueCAN</li></ul> | Devices that use a USB connection listed here have a virtual COM port connection to the PC even though it is connected to the USB port on the PC. |
| USB            | <ul><li>neoVI Green</li></ul>                                                                                                                   | These devices use the USB Port type                                                                                                               |
| TCP/IP         | <ul><li>neoVI Blue</li><li>neoVI Pro</li><li>neoVI Green</li><li>ValueCAN</li></ul>                                                             | All ICS devices can be connected via a TCP/IP connection using a second PC as a gateway.                                                          |
