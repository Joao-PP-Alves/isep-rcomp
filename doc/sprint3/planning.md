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
- Building A: area 1
- Building B: area 2
- Building C: area 3
- Building D: area 4

The prefixes for the phones will follow the same pattern:
- Building A: 1... (1001, 1002, ...)
- Building B: 2... (2001, 2002, ...)
- Building C: 3... (3001, 3002, ...)
- Building D: 4... (4001, 4002, ...)

DNS domain for all the buildings:
- Building A: rcomp-19-20-dd-g5 / ns.rcomp-19-20-dd-g5
- Building B: building-2.rcomp-19-20-dd-g5 / ns.building-2.rcomp-20-21-dd-g5
- Building C: building-3.rcomp-19-20-dd-g5 / ns.building-3.rcomp-19-20-dd-g5
- Building D: building-4.rcomp-19-20-dd-g5 / ns.building-4.rcomp-19-20-dd-g5

# 3. Subtasks assignment #

  * 1191513 - (T.3.3) Update the campus.pkt layer three Packet Tracer simulation from the
previous sprint, to include the described features in this sprint for building C.

  * 1190743 - (T.3.2) Update the campus.pkt layer three Packet Tracer simulation from the
previous sprint, to include the described features in this sprint for building B.

  * 1182147 - (T.3.1) Update the campus.pkt layer three Packet Tracer simulation from the previous sprint, to include the described features in this sprint for building A.

  * 1170640 - (T.3.4) Update the campus.pkt layer three Packet Tracer simulation from the
previous sprint, to include the described features in this sprint for building D + Final integration of each member’s Packet Tracer simulation into a single simulation.

# 4. Notes # 

- The final integration was delegated to the member of building 4, as it was the sprint master.
