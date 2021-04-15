RCOMP 2020-2021 Project - Sprint 2 - Member 1191513 folder
===========================================

## General Information
- End user outlets on the ground floor: 60 nodes
- End user outlets on floor one: 70 nodes
- Wi-Fi network: 100 nodes
- Local servers and administration workstations (DMZ): 12 nodes
- VoIP (IP-phones): 35 nodes
- Backbone: 120 nodes

## Distribution

- VTP Domain: rcompddg5.
- The addresses range of Building 1 is 10.122.208.0 to 10.122.209.255.

| VLAN ID | VLAN Name | Subnet Address  | Net Mask  | Available Address Range  |  Broadcast Address | Available IPs |
|---|---|---|---|---|---|---|
| 135 | rcompddg5_B1_BackBone | 10.122.208.0/25   | 255.255.255.128 | 10.122.208.1 - 10.122.208.126   | 10.122.208.127 | 126 |
| 136 | rcompddg5_B1_floor_0  | 10.122.208.128/26 | 255.255.255.192 | 10.122.208.129 - 10.122.208.190 | 10.122.208.191 | 62  |
| 137 | rcompddg5_B1_floor_1  | 10.122.208.192/26 | 255.255.255.192 | 10.122.208.193 - 10.122.208.254 | 10.122.208.191 | 62  |
| 138 | rcompddg5_B1_WiFi     | 10.122.209.224/27 | 255.255.255.224 | 10.122.209.225 - 10.122.208.254 | 10.122.208.255 | 30  |
| 139 | rcompddg5_B1_DMZ      | 10.122.209.0/25   | 255.255.255.128 | 10.122.209.1 - 10.122.208.126   | 10.122.208.127 | 126 |
| 140 | rcompddg5_B1_VoIP     | 10.122.209.192/27 | 255.255.255.224 | 10.122.209.192 - 10.122.208.222 | 10.122.208.223 | 30  |



