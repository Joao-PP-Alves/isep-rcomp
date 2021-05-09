RCOMP 2020-2021 Project - Sprint 3 planning
===========================================
### Sprint master: 1170640 (Ricardo Mourisco) ###

# 1. Sprint's backlog #

In this sprint the team is required to elaborate some tasks:
1. OSPF dynamic routing
2. HTTP servers
3. DHCPv4 service
4. VoIP service
5. DNS
6. NAT (Network Address Translation)
7. Static Firewall (ACLs)

All these tasks must be accomplished usint the previous sprint's packet tracker file for the campus.

Each team-member will deliver that file with all the configurations reagarding their building.

# 2. Technical decisions and coordination #

We will name our ospf 'ospf 1' and the areas will be distributed by buildings so:
- Building 1: area 1
- Building 2: area 2
- Building 3: area 3
- Building 4: area 4

The prefixes for the phones will follow the same pattern:
- Building 1: 1... (1001, 1002, ...)
- Building 2: 2... (2001, 2002, ...)
- Building 3: 3... (3001, 3002, ...)
- Building 4: 4... (4001, 4002, ...)

DNS domain for all the buildings:
- Building 1: rcomp-19-20-dd-g5 / ns.rcomp-19-20-dd-g5
- Building 2: building-2.rcomp-19-20-dd-g5 / ns.building-2.rcomp-20-21-dd-g5
- Building 3: building-3.rcomp-19-20-dd-g5 / ns.building-3.rcomp-19-20-dd-g5
- Building 4: building-4.rcomp-19-20-dd-g5 / ns.building-4.rcomp-19-20-dd-g5

# 3. Subtasks assignment #

  * 1191513 - (T.3.3) Update the campus.pkt layer three Packet Tracer simulation from the
previous sprint, to include the described features in this sprint for building 3.

  * 1190743 - (T.3.2) Update the campus.pkt layer three Packet Tracer simulation from the
previous sprint, to include the described features in this sprint for building 2.

  * 1182147 - (T.3.1) Update the campus.pkt layer three Packet Tracer simulation from the previous sprint, to include the described features in this sprint for building 1.

  * 1170640 - (T.3.4) Update the campus.pkt layer three Packet Tracer simulation from the
previous sprint, to include the described features in this sprint for building 4 + Final integration of each member’s Packet Tracer simulation into a single simulation.

# 4. Notes #

- The final integration was delegated to the member of building 4, as it was the sprint master.
