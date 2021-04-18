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

| VTP Domain  | VLAN ID | Subnet Address  | Net Mask  | Available Address Range  |  Broadcast Address | Gateway Address | 
|---|---|---|---|---|---|---|
| rcompddg5_B2_floor_0 | 142  | 10.122.210.128/26  | 255.255.255.192  | 10.122.210.129 - 10.122.210.190  | 10.122.210.191 | 10.122.210.129 |
| rcompddg5_B2_floor_1 | 141  | 10.122.210.0/25   | 255.255.255.128  | 10.122.210.1 - 10.122.210.126  | 10.122.210.127 | 10.122.210.1 |
| rcompddg5_B2_WiFi |  144 | 10.122.211.0/25  | 255.255.255.128 | 10.122.211.1 - 10.122.211.126  | 10.122.211.127 | 10.122.211.1 |
| rcompddg5_B2_DMZ |  143 | 10.122.210.192/28  | 255.255.255.240 | 10.122.210.193 - 10.122.210.206  |  10.122.210.207 | 10.122.210.193 |
| rcompddg5_B2_VoIP |  145 | 10.122.211.128/26 | 255.255.255.192  | 10.122.211.129 - 10.122.211.190  | 10.122.210.191  | 10.122.211.129 |


## Configurations on Packet Tracer

- VLANS were added to the **Dummy_Connection** Database (135 to 155), as the **Dummy_Connection** is the server (replacing the backbone) and should replicate the database to all layer 2 devices.
- ICC interfaces set to trunk mode.
- HCC interfaces set to:
    - Trunk mode if connected to other Switch.
    - Access mode if connected to end user device.
- End devices were connected to the HCCs or CPs using Copper patch cables.
- Redundancy between ICCs and HCCs was taken into consideration, but not by connecting 2 cables in the .pkt file.
- SSIDs and authentication modes on Access Points were not setup since it was not asked for Sprint2.
- IP Addresses assigned to all end devices.
- Laptops, DMZ Server and VoIP phone connected to respective HCC or CP.
