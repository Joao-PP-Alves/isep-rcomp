RCOMP 2020-2021 Project - Sprint 3 - Member 1191513 folder
===========================================

# Building 1

#### Distribution (from previous sprint)

- VTP Domain: rcompddg5.
- The addresses range of Building 1 is 10.122.208.0 to 10.122.209.255.
- VLANID range from 135 to 140.

| VLAN ID | VLAN Name | Subnet Address  | Net Mask  | Available Address Range  |  Broadcast Address | Available IPs | Gateway Address | 
|---|---|---|---|---|---|---| --- | 
| 135 | rcompddg5_B1_BackBone | 10.122.208.0/25   | 255.255.255.128 | 10.122.208.1 - 10.122.208.126   | 10.122.208.127 | 126 | 10.122.208.1 |
| 136 | rcompddg5_B1_floor_0  | 10.122.208.128/26 | 255.255.255.192 | 10.122.208.129 - 10.122.208.190 | 10.122.208.191 | 62  | 10.122.208.129 | 
| 137 | rcompddg5_B1_floor_1  | 10.122.208.192/26 | 255.255.255.192 | 10.122.208.193 - 10.122.208.254 | 10.122.208.191 | 62  | 10.122.208.193 | 
| 138 | rcompddg5_B1_WiFi     | 10.122.209.224/27 | 255.255.255.224 | 10.122.209.225 - 10.122.208.254 | 10.122.208.255 | 30  | 10.122.209.225 |
| 139 | rcompddg5_B1_DMZ      | 10.122.209.0/25   | 255.255.255.128 | 10.122.209.1 - 10.122.208.126   | 10.122.208.127 | 126 | 10.122.209.1 |
| 140 | rcompddg5_B1_VoIP     | 10.122.209.192/27 | 255.255.255.224 | 10.122.209.193 - 10.122.208.222 | 10.122.208.223 | 30  | 10.122.209.193 | 


## Comands for router configuration ##

#### DHCP ####

    ip dhcp excluded-address 10.122.208.1
    ip dhcp excluded-address 10.122.208.129
    ip dhcp excluded-address 10.122.208.193
    ip dhcp excluded-address 10.122.209.225
    ip dhcp excluded-address 10.122.209.193
    
    ip dhcp pool VLAN135
    network 10.122.208.0 255.255.255.128
    default-router 10.122.210.1
    dns-server 10.122.209.2
    domain-name building-1.rcomp-20-21-dd-g5

    ip dhcp pool VLAN136
    network 10.122.208.128 255.255.255.192
    default-router 10.122.210.129
    dns-server 10.122.209.2
    domain-name building-1.rcomp-20-21-dd-g5
    
    ip dhcp pool VLAN137
    network 10.122.208.192 255.255.255.192
    default-router 10.122.208.193
    dns-server 10.122.209.2
    domain-name building-1.rcomp-20-21-dd-g5

    ip dhcp pool VLAN138
    network 10.122.209.224 255.255.255.224
    default-router 10.122.209.225
    dns-server 10.122.209.2
    domain-name building-1.rcomp-20-21-dd-g5

    ip dhcp pool VLAN140
    network 10.122.209.192 255.255.255.224
    default-router 10.122.209.193
    option 150 ip 10.122.209.193
    dns-server 10.122.209.2
    domain-name building-1.rcomp-20-21-dd-g5

#### VLAN ####

    interface FastEthernet1/0.136
    description rcompddg5_B1_floor_0
    encapsulation dot1Q 136
    ip address 10.122.208.129 255.255.255.192

    interface FastEthernet1/0.137
    description rcompddg5_B1_floor_1
    encapsulation dot1Q 137
    ip address 10.122.208.193 255.255.255.192

    interface FastEthernet1/0.138
    description rcompddg5_B1_WiFi
    encapsulation dot1Q 138
    ip address 10.122.209.225 255.255.255.224

    interface FastEthernet1/0.139
    description rcompddg5_B1_DMZ
    encapsulation dot1Q 139
    ip address 10.122.209.1 255.255.255.128

    interface FastEthernet1/0.140
    description rcompddg5_B1_VoIP
    encapsulation dot1Q 140
    ip address 10.122.209.193 255.255.255.224


#### OSPF ####

    router ospf 1
    log-adjacency-changes
    network 10.122.208.0 0.0.1.255 area 1


#### NAT ####

    ip nat inside source static tcp 10.122.209.3 80 10.122.208.0 80
    ip nat inside source static tcp 10.122.209.3 443 10.122.208.0 443
    ip nat inside source static tcp 10.122.209.2 53 120.57.208.186 53
    ip nat inside source static udp 10.122.209.2 53 120.57.208.186 53 


#### VoiP ####

    dial-peer voice 2000 voip
    destination-pattern 2...
    session target ipv4:10.122.211.129

    dial-peer voice 3000 voip
    destination-pattern 3...
    session target ipv4:10.122.212.193

    dial-peer voice 4000 voip
    destination-pattern 4...
    session target ipv4:10.122.214.193

    telephony-service
    max-ephones 20
    max-dn 20
    ip source-address 10.122.209.193 port 2000
    auto assign 1 to 2

    ephone-dn 1
    number 1001

    ephone-dn 2
    number 1002

    ephone 1
    device-security-mode none
    mac-address 0001.648E.41D9
    type 7960
    button 1:1

    ephone 2
    device-security-mode none
    mac-address 0090.0CDD.DC41
    type 7960
    button 1:2
