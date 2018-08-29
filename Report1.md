# Crossover Networking
- This type of network will be using a **crossover cable** for Ethernet to connect computer devices  together **directly**.  Usually used to connect 2 devices of the **same** type.
- Crossover means **the order of the two pairs have to be different**. Therefore, we have two type of the cable head which are **T568A** and **T568B**.

**T568A**:
|Pin#|  1|  2|  3|  4|  5|  6|  7|  8|
|----|---|---|---|---|---|---|---|---|
|   |White/ Green| Green | White/ Orange| Blue| White/ Blue| Orange| White/ Brown|Brown|

**T568B**:
|Pin#|  1|  2|  3|  4|  5|  6|  7|  8|
|----|---|---|---|---|---|---|---|---|
|   |White/ Orange| Orange | White/ Green| Blue| White/ Blue| Green| White/ Brown|Brown|

# Preparation
- 2 Computers.
- A crossover network cable

# Setup the Network
1. Connecting 2 computers using the crossover cable.
2. Go to **Control Panel** -> **Networking and Sharing Center**.
3. Click to the **Ethernet** connection, then choose **Properties** -> **TCP/IPv4** -> **Properties**.
4. Checking **Use the following IP address** then input:

|COM#|1 |2 |
|--|--|--|
|**IP Address**|192.168.253.1| 192.168.253.2|
| **Subnet Mask** |255.255.255.0| 255.255.255.0|
|**Default Gateway**|192.168.1.99|192.168.253.1|
|**DNS Server**|8.8.8.8|8.8.8.8|
5. Click **OK** to save the **manually inputted **.
6. Back to **Networking and Sharing Center** -> **Change advance sharing settings**.
7. In **Guest**, **Public**, and **All Networks** check **Turn on Network discovery** and **Turn on file and printers sharing** then **Save change**.
8. Back to **Control Panel** -> **Window Firewall** -> **Customize settings for each type of the Network**.
9. **TURN OFF** firewall at private and public Network on both Computers.
10. Open **Command line** on both computers to test the connection.
11. On Computer 1 **Command line** type:
	ping 192.168.0.2
	  On Computer 2 **Command line** type:
	ping 192.168.0.1
	By doing this, we are trying to see does computer 1 can connect to computer 2 or not and from computer 2 to computer 1.
12. You can also share the internet connection to the other computer as well.
**Situation**: Computer 1 have a wireless access to the internet and we want to share it to computer 2. We can do this by going to the **Network Connection and Internet** -> **Network Connection**
+ Right click on the **Wireless Connection** the choose **Properties**
+ In **Sharing** task, check **Allow other network users to connect through this computer's internet connection** then choose **Local Area Connection** then click **OK** to save it.

# Connection Map

Com2  <---------------------------------> Com1 <----------------------------> Internet
| IP Address |  Com2  <-> Com1 | Com1 <-> Internet |
|--|--|--|
|  | 192.168.0.2 <-> 192.168.0.1 | 192.168.1.99 <-> Internet
