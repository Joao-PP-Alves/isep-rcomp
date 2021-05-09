RCOMP 2020-2021 Project - Sprint 3 - Member 1190743 folder
===========================================
# Building 2

## Decisions ##

 - DNS server will be the server already existing in the previous sprint, while the HTTP server will be the new one;
 - VoiP phones will have numbers from 2000+ to 2999;
 - The area of this building will have the same digit as the building itself: **2**;
 - This building will have a maximum of 20 VoiP phones;
 - Domain-name will be **building-2.rcomp-20-21-dd-g5**;
 - The DMZ network will not change to a DHCP connection, since the servers will be connected statically.

## Comands ##

#### DHCP ####

    ip dhcp excluded-address 10.122.210.129
    ip dhcp excluded-address 10.122.210.1
    ip dhcp excluded-address 10.122.211.1
    ip dhcp excluded-address 10.122.211.129
    
    ip dhcp pool VLAN142 
    network 10.122.210.128 255.255.255.192
    default-router 10.122.210.129
    dns-server 10.122.210.194
    domain-name building-2.rcomp-20-21-dd-g5

    ip dhcp pool VLAN141
    network 10.122.210.0 255.255.255.128
    default-router 10.122.210.1
    dns-server 10.122.210.194
    domain-name building-2.rcomp-20-21-dd-g5

    ip dhcp pool VLAN144
    network 10.122.211.0 255.255.255.128
    default-router 10.122.211.1
    dns-server 10.122.210.194
    domain-name building-2.rcomp-20-21-dd-g5

    ip dhcp pool VLAN145
    network 10.122.211.128 255.255.255.192
    default-router 10.122.211.129
    option 150 ip 10.122.211.129
    dns-server 10.122.210.194
    domain-name building-2.rcomp-20-21-dd-g5

#### VLAN ####

    interface FastEthernet1/0.1
    encapsulation dot1Q 142
    ip address 10.122.210.129 255.255.255.192

    interface FastEthernet1/0.2
    encapsulation dot1Q 141
    ip address 10.122.210.1 255.255.255.128

    interface FastEthernet1/0.3
    encapsulation dot1Q 144
    ip address 10.122.211.1 255.255.255.128

    interface FastEthernet1/0.4
    encapsulation dot1Q 143
    ip address 10.122.210.193 255.255.255.240

    interface FastEthernet1/0.5
    encapsulation dot1Q 145
    ip address 10.122.211.129 255.255.255.192

#### OSPF ####

    router ospf 1
    log-adjacency-changes
    network 10.122.210.0 0.0.1.255 area 2


#### VoiP ####

    dial-peer voice 1000 voip
    destination-pattern 1...
    session target ipv4:10.166.137.161

    dial-peer voice 3000 voip
    destination-pattern 3...
    session target ipv4:10.122.212.193

    dial-peer voice 4000 voip
    destination-pattern 4...
    session target ipv4:10.122.214.193

    telephony-service
    max-ephones 20
    max-dn 20
    ip source-address 10.122.211.129 port 2000
    auto assign 1 to 2

    ephone-dn 1
    number 2001

    ephone-dn 2
    number 2002

    ephone 1
    device-security-mode none
    mac-address 000C.8514.7A7D
    type 7960
    button 1:1

    ephone 2
    device-security-mode none
    mac-address 0060.5C37.310B
    type 7960
    button 1:2
    

#### NAT ####
    
    ip nat inside source static tcp 10.122.210.194 80 10.122.208.0 8081 
    ip nat inside source static tcp 10.122.210.194 443 10.122.208.0 8082
