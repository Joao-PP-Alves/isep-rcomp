RCOMP 2020-2021 Project - Sprint 2 - Member 1170640 folder
===========================================

## General Information
- End user outlets on the ground floor: 40 nodes
- End user outlets on floor one: 50 nodes
- Wi-Fi network: 60 nodes
- Local servers, administration workstations, and industrial machines (DMZ): 250 nodes
- VoIP (IP-phones): 25 nodes


## Distribuction

The range of addresses to my building is 10.122.214.0 to 10.122.215.255.

| VTP Domain  | VLAN ID | Subnet Address  | Net Mask  | Available Address Range  |  Broadcast Address |
|---|---|---|---|---|---|
| rcompddg5_B2_floor_0 | 151  | 10.122.214.0/26 | 255.255.255.192  | 10.122.214.1 - 10.122.214.62  | 10.122.214.63  |
| rcompddg5_B2_floor_1 | 152  | 10.122.214.64/26   | 255.255.255.192  | 10.122.214.65 - 10.122.214.126  | 10.122.214.127 |
| rcompddg5_B2_WiFi |  153 | 10.122.214.128/26  | 255.255.255.192 | 10.122.214.129 - 10.122.214.190  | 10.122.214.191 |
| rcompddg5_B2_DMZ |  154 | 10.122.215.0/24  | 255.255.255.0 | 10.122.215.1 - 10.122.215.254  |  10.122.215.255 |
| rcompddg5_B2_VoIP |  155 | 10.122.214.192/26 | 255.255.255.192  | 10.122.214.193 - 10.122.214.254  | 10.122.214.255  |