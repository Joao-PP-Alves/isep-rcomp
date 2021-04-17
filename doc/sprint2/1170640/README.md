RCOMP 2020-2021 Project - Sprint 2 - Member 1170640 folder
===========================================

## Building 4

For this Sprint, I was in charge of the development of a layer two and layer three Packet Tracer simulation for building 4, and also encompassing the campus backbone.

## General Information
- End user outlets on the ground floor: 40 nodes
- End user outlets on floor one: 50 nodes
- Wi-Fi network: 60 nodes
- Local servers, administration workstations, and industrial machines (DMZ): 250 nodes
- VoIP (IP-phones): 25 nodes

## Distribuction

- VTP Domain: rcompddg5.
- VLANID range from 151 to 155.
- The range of addresses to my building is 10.122.214.0 to 10.122.215.255.

| VTP Domain  | VLAN ID | Subnet Address  | Net Mask  | Available Address Range  |  Broadcast Address |
|---|---|---|---|---|---|
| rcompddg5_B4_floor_0 | 151  | 10.122.214.0/26 | 255.255.255.192  | 10.122.214.1 - 10.122.214.62  | 10.122.214.63  |
| rcompddg5_B4_floor_1 | 152  | 10.122.214.64/26   | 255.255.255.192  | 10.122.214.65 - 10.122.214.126  | 10.122.214.127 |
| rcompddg5_B4_WiFi |  153 | 10.122.214.128/26  | 255.255.255.192 | 10.122.214.129 - 10.122.214.190  | 10.122.214.191 |
| rcompddg5_B4_DMZ |  154 | 10.122.215.0/24  | 255.255.255.0 | 10.122.215.1 - 10.122.215.254  |  10.122.215.255 |
| rcompddg5_B4_VoIP |  155 | 10.122.214.192/26 | 255.255.255.192  | 10.122.214.193 - 10.122.214.254  | 10.122.214.255  |

## Configurations on Packet Tracer

- VLANS were added to the **Dummy_Connection** Database (135 to 155), as the **Dummy_Connection** is the server (replacing the backbone) and should replicate the database to all layer 2 devices.
- IC interfaces set to trunk mode.
- HC interfaces set to:
    - Trunk mode if connected to other Switch.
    - Access mode if connected to a access point.
- CP interfaces set to:
    - Trunk mode to other switches
    - Access mode to all other devices as they're the end point to where users will connect to.
- Except for the VoIP phones, all other end devices have a static and manually defined IPv4 configuration, including the default gateway.
- All end devices are connected to their proper and respective VLANs.
- End devices were connected to the CPs using Copper patch cables.
- SSIDs and authentication modes on Access Points were not setup since it was not asked for Sprint2.
- Laptops, Workstations, DMZ Server and VoIP phone connected to respective CPs (and in case of the laptops, access points).
