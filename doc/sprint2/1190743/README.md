RCOMP 2020-2021 Project - Sprint 2 - Member 1190743 folder
===========================================

## General Information
- End user outlets on the ground floor: 60 nodes
- End user outlets on floor one: 70 nodes
- Wi-Fi network: 100 nodes
- Local servers and administration workstations (DMZ): 12 nodes
- VoIP (IP-phones): 35 nodes


## Distribuction

The range of addresses to my building is 10.122.210.0 to 10.122.211.255.

| VTP Domain  | VLAN ID | Subnet Address  | Net Mask  | Available Address Range  |  Broadcast Address |
|---|---|---|---|---|---|
| rcompddg5_B2_floor_0 | 142  | 10.122.210.128/26  | 255.255.255.192  | 10.122.210.129 - 10.122.210.190  | 10.122.210.191  |
| rcompddg5_B2_floor_1 | 141  | 10.122.210.0/25   | 255.255.255.128  | 10.122.210.1 - 10.122.210.126  | 10.122.210.127 |
| rcompddg5_B2_WiFi |  144 | 10.122.211.0/25  | 255.255.255.128 | 10.122.211.1 - 10.122.211.126  | 10.122.211.127 |
| rcompddg5_B2_DMZ |  143 | 10.122.210.192/28  | 255.255.255.240 | 10.122.210.193 - 10.122.210.206  |  10.122.210.207 |
| rcompddg5_B2_VoIP |  145 | 10.122.211.128/26 | 255.255.255.192  | 10.122.211.129 - 10.122.211.190  | 10.122.210.191  |

