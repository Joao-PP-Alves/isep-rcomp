RCOMP 2020-2021 Project - Sprint 2 - Member 1182147 folder
===========================================

## Building 3

For this particular Sprint, I was in charge of the development of a layer two and layer three Packet Tracer simulation for building 3, and also encompassing the campus backbone.

## Glossary

 - VTP -> VLAN Trunk Protocol
 - VoIP -> Voice over Internet Protocol
 - VLAN -> Virtual Local Area Network
 - WiFi -> Wireless Fidelity
 - ICC -> Intermediate Cross-Connect
 - HCC -> Horizontal Cross-Connect
 - CP -> Consolidation Point
 - IPv4 -> Internet Protocol version 4
 - SSID -> Service Set Identifier

## General Information

- End user outlets on the ground floor: 40 nodes
- End user outlets on floor one: 44 nodes
- Wi-Fi network: 60 nodes
- Local servers and administration workstations (DMZ): 250 nodes
- VoIP (IP-phones): 40 nodes

## Distribution

 - VTP Domain: rcompddg5.
 - The range of addresses to my building is 10.122.212.0 to 10.122.213.255.
 - VLANID range from 146 to 150.

| VTP Domain  | VLAN ID | Subnet Address  | Net Mask  | Available Address Range  |  Broadcast Address |
|---|---|---|---|---|---|
| rcompddg5_B3_floor_0 | 146 | 10.122.212.0/26   | 255.255.255.192 | 10.122.212.1 - 10.122.212.62    | 10.122.214.63  |
| rcompddg5_B3_floor_1 | 147 | 10.122.212.64/26  | 255.255.255.192 | 10.122.212.65 - 10.122.212.126  | 10.122.214.127 |
| rcompddg5_B3_WiFi    | 148 | 10.122.212.128/26 | 255.255.255.192 | 10.122.212.129 - 10.122.212.190 | 10.122.214.191 |
| rcompddg5_B3_DMZ     | 149 | 10.122.213.0/24   |  255.255.255.0  | 10.122.213.1 - 10.122.213.254   | 10.122.215.255 |
| rcompddg5_B3_VoIP    | 150 | 10.122.212.192/26 | 255.255.255.192 | 10.122.212.193 - 10.122.212.254 | 10.122.214.255 |


## Configurations on Packet Tracer

- VLANS were added to the **Dummy_Connection** Database (135 to 155), as the **Dummy_Connection** is the server (replacing the backbone) and should replicate the database to all layer 2 devices.
- ICC interfaces set to trunk mode.
- HCC interfaces set to:
    - Trunk mode if connected to other Switch.
    - Access mode if connected to end user device.
    - In regards to VoIP, the corresponding port on the switch was configured in Access mode. However, the Access VLAN was disabled and instead the Voice VLAN was used.
- CP interfaces set to Access mode as they're solely connected to end user devices.
- Except for the VoIP phones, all other end devices have a static and manually defined IPv4 configuration, including the default gateway.
- All end devices are connected to their proper and respective VLANs.
- End devices were connected to the HCCs or CPs using Copper patch cables.
- Redundancy between ICCs and HCCs was taken into consideration, but not by connecting 2 cables in the .pkt file.
- SSIDs and authentication modes on Access Points were not setup since it was not asked for Sprint2.
- Workstations, Laptops, DMZ Server and VoIP phone connected to respective HCC or CP.
