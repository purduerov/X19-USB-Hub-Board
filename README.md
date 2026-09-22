# Purdue ROV X19 USB Hub Board

This board acts as both a PCIe-USB host controller and USB hub board for the ROV stack. In previous years, we had off-the-shelf USB hubs plugged in to the stock ports on the Raspberry Pi. We ran into multiple issues - there were bandwidth allocation issues with the default controller and the hub was just sitting on top of the stack in the enclosure.

The board uses a Renesas uPD720201 USB3.0 host controller to interface with the Raspberry Pi. That takes the PCIe 2.0 x1 interface and makes 4x USB 3.0 ports. Each of those ports (routed 2.0 since 3.0 bandwidth is not required) then go into a USB2422 hub controller and get split into 2 ports, for a total of 8 with 240 Mbps (30 MB/s) dedicated bandwidth.