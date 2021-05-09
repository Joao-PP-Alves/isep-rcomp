RCOMP 2020-2021 Project - Sprint 3 - Member 1182147 folder
===========================================

## Glossary

 - OSPF - Open Shortest Path First
 - DHCPv4 - Dynamic Host Configuration Protocol version 4
 - VoIP - Voice over Internet Protocol
 - DMZ - Demilitarized Zone
 - HTTP - Hypertext Transfer Protocol
 - DNS - Domain Name System
 - NAT - Network Address Translation

## Building 3

For this particular Sprint, we were expected to implement the following configurations:

 - OSPF based dynamic routing
 - DHCPv4 service
 - VoIP service
 - Adding a second server to each DMZ network to run the HTTP service.
 - Configuring DNS servers to establish a DNS domains tree.
 - Enforcing NAT (Network Address Translation).
 - Establishing traffic access policies on routers (static firewall).

## OSPF COMMANDS

router ospf 1
 log-adjacency-changes
 network 10.122.212.0 0.0.1.255 area 3

## DHCP / DNS COMMANDS

ip dhcp excluded-address 10.122.212.1
ip dhcp excluded-address 10.122.212.65
ip dhcp excluded-address 10.122.212.129
ip dhcp excluded-address 10.122.212.193

ip dhcp pool VLAN146
 network 10.122.212.0 255.255.255.192
 default-router 10.122.212.1
 dns-server 10.122.213.2
 domain-name building-3.rcomp-20-21-dd-g5

ip dhcp pool VLAN147
 network 10.122.212.64 255.255.255.192
 default-router 10.122.212.65
 dns-server 10.122.213.2
 domain-name building-3.rcomp-20-21-dd-g5

ip dhcp pool VLAN148
 network 10.122.212.128 255.255.255.192
 default-router 10.122.212.129
 dns-server 10.122.213.2
 domain-name building-3.rcomp-20-21-dd-g5

ip dhcp pool VLAN150
 network 10.122.212.192 255.255.255.192
 default-router 10.122.212.193
 option 150 ip 10.122.212.193
 dns-server 10.122.213.2
 domain-name building-3.rcomp-20-21-dd-g5

## VoIP COMMANDS

dial-peer voice 1000 voip
 destination-pattern 1...
 session target ipv4:10.122.209.193

dial-peer voice 2000 voip
 destination-pattern 2...
 session target ipv4:10.122.211.129

dial-peer voice 4000 voip
 destination-pattern 4...
 session target ipv4:10.122.214.193

telephony-service
 max-ephones 40
 max-dn 40
 ip source-address 10.122.212.193 port 2000
 auto assign 11 to 12

ephone-dn 11
 number 3001

ephone-dn 12
 number 3002

ephone 1
 device-security-mode none
 mac-address 0000.0CB5.C09C
 type 7960
 button 1:12

ephone 2
 device-security-mode none
 mac-address 0060.5CD0.35C4
 type 7960
 button 1:11

## DNS

![DNS.png](DNS.png)

## NAT COMMANDS

ip nat inside source static tcp 10.122.213.3 80 120.57.210.186 80
ip nat inside source static tcp 10.122.213.3 443 120.57.210.186 443
ip nat inside source static tcp 10.122.213.2 53 120.57.210.186 53
ip nat inside source static udp 10.122.213.2 53 120.57.210.186 53
