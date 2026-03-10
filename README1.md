<div align="center">

# 🛡️ Computer and Network Security  
### Cisco Show Commands Guide

📚 Basic monitoring and troubleshooting commands used in Cisco Router and Switch devices.

</div>

---

## 📑 Table of Contents

- [Configuration Commands](#configuration-commands)
- [Interface Commands](#interface-commands)
- [System Commands](#system-commands)
- [Network Commands](#network-commands)
- [Switch Commands](#switch-commands)
- [Monitoring Commands](#monitoring-commands)

---

# 🔧 Configuration Commands

| Command | Description |
|------|------|
| `show running-config` | Displays the current running configuration stored in RAM |
| `show startup-config` | Displays the configuration stored in NVRAM |

---

## 1️⃣ show running-config

📌 **Displays the current configuration of the device**

Shows the configuration currently running in **RAM**.  
Any configuration changes that are not saved will appear here.

```bash
Router# show running-config
2️⃣ show startup-config

📌 Displays the startup configuration

Shows the configuration stored in NVRAM that loads when the device boots.

Router# show startup-config
🌐 Interface Commands
Command	Purpose
show ip interface brief	Shows a summary of interface status
show interfaces	Displays detailed interface statistics
3️⃣ show ip interface brief

📌 Displays a summary of all interfaces

Shows:

IP address

Interface status

Protocol status

Router# show ip interface brief

Example Output

Interface              IP-Address      OK? Method Status                Protocol
FastEthernet0/0       192.168.1.1     YES manual up                    up
FastEthernet0/1       unassigned      YES unset  administratively down down
4️⃣ show interfaces

📌 Displays detailed interface statistics

Includes:

Bandwidth

Packet statistics

Error counts

Traffic details

Router# show interfaces FastEthernet0/0
🖥️ System Commands
Command	Description
show version	Displays system information
show clock	Displays device time
show processes	Shows running processes and CPU usage
5️⃣ show version

Displays system information such as:

IOS version

uptime

processor type

memory information

Router# show version

Example

Cisco IOS Software, Version 12.4
System uptime is 2 hours, 30 minutes
Processor board ID FTX1234A1BC
6️⃣ show clock

Displays the current system time and date.

Router# show clock
7️⃣ show processes

Displays CPU usage and running processes.

Router# show processes
🔀 Network Commands
Command	Description
show ip route	Displays routing table
show arp	Displays ARP table
8️⃣ show ip route

Displays the router’s routing table.

Router# show ip route
9️⃣ show arp

Displays IP to MAC address mappings.

Router# show arp

Example

Protocol  Address          Age (min)  Hardware Addr   Type   Interface
Internet  192.168.1.10     2          00:1A:2B:3C:4D:5E  ARPA   FastEthernet0/0
🔁 Switch Commands
Command	Description
show mac address-table	Displays learned MAC addresses
show vlan brief	Displays VLAN configuration
🔟 show mac address-table

Displays MAC addresses learned by the switch.

Switch# show mac address-table
1️⃣1️⃣ show vlan brief

Displays VLAN information.

Switch# show vlan brief

Example

VLAN Name                             Status    Ports
1    default                          active    Fa0/1, Fa0/2
10   Sales                            active    Fa0/3, Fa0/4
20   IT                               active    Fa0/5, Fa0/6
📊 Monitoring Commands
Command	Description
show logging	Displays system logs
show users	Displays connected users
show history	Displays command history
show flash	Displays flash memory files
1️⃣2️⃣ show logging

Displays device log messages.

Router# show logging
1️⃣3️⃣ show users

Displays users currently connected to the device.

Router# show users
1️⃣4️⃣ show history

Displays previously entered commands.

Router# show history
1️⃣5️⃣ show flash

Displays files stored in flash memory.

Router# show flash
<div align="center">

⭐ Computer and Network Security Notes
📡 Cisco Router & Switch CLI Commands

</div> ```
