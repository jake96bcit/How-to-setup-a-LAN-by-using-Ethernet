# Straight Networking
- This type of network will be using a **Straight cable** for Ethernet to connect computer devices  together **through a hub**. Usually used to connect many devices of the **different** types.
- Example:
    1) Connect a **computer** to a **switch/hub**'s normal port.
    2) Connect a **computer** to a **cable/DSL modem**'s LAN port.
    3) Connect a **router**'s WAN port to a **cable/DSL modem**'s LAN port.
    4) Connect a **router**'s LAN port to a **switch/hub**'s uplink port. (normally used for expanding network)
    5) Connect 2 **switch/hubs** with one of the **switch/hub** using an **uplink** port and the other one using normal port.
- Both side (side A and side B) of **straight** cable have wire arrangement with same colors.

|Pin#|  1|  2|  3|  4|  5|  6|  7|  8|
|----|---|---|---|---|---|---|---|---|
|   |White/ Orange| Orange | White/ Green| Blue| White/ Blue| Green| White/ Brown|Brown|

# Preparation
- 2 Computers.
- 2 straight network cables.
- A switch/hubs.
- A router that connected to the internet.

# Setup the Network
1. Connecting 2 computers to the switch/hubs using the straight cables.
2. Go to **Control Panel** -> **Networking and Sharing Center**.
3. Click to the **Ethernet** connection, then choose **Properties** -> **TCP/IPv4** -> **Properties**.
4. Making sure that we are using **DHCP/Automatically** on both computer. This time, your IP addresses will be offered by the Internet provider.
5. Back to the **Properties** of the **Ethernet** then click **Details**.
6. Back to **Networking and Sharing Center** -> **Change advance sharing settings** to see what is the IP address of the computer (In here we are checking on both computers, **they should be different**).
7. In **Guest**, **Public**, and **All Networks** check **Turn on Network discovery** and **Turn on file and printers sharing** then **Save change**.
8. Back to **Control Panel** -> **Window Firewall** -> **Customize settings for each type of the Network**.
9. **TURN OFF** firewall at private Network on both Computers.
10. Open **Command line** on both computers to test the connection.
11. On Computer 1 **Command line** type:

	`ping (The IP address of Computer 2)`

	  On Computer 2 **Command line** type:

	`ping (The IP address of Computer 1)`

	Then On both computer, type:

	`ping 8.8.8.8`

	(8.8.8.8 is google DNS)
	By doing this, we are trying to see does computer 1 can connect to computer 2 or not, from computer 2 to computer 1, and whether these computers can connect to the internet or not by.

# Connection Map

Com1 <---------------------------------->| HUB |<----------------------------> Internet
Com2 <---------------------------------->| HUB |
(Other devices) <----------------------->| HUB |

<div class='mermaid'>
LR
A[Com1] -->D[Hub];
    B[Com2] --> D[Hub];
    C[Other Devices] --> D[Hub];
    D -->E[Internet];
</div>
