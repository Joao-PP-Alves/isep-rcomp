RCOMP 2020-2021 Project - Sprint 2 planning
===========================================
### Sprint master: João Alves - 1190743 ###

# 1. Sprint's backlog #
Regarding Sprint 2, this team is now, using the last project made, asked to create a network simulation (using Cisco Packet Tracer).
In terms of knowledge, the focus is on the layer two infrastructure and the layer three fundamentals, such as IPv4 addressing and static routing.
On this document are specified the common technical decisions for all the buildings to follow. These were decided in group and will be explained ahead.

# 2. Technical decisions and coordination #

* To a better understanding and consistency of the project, improving from our last sprint, we decided that all information displayed on the files will be in English.

* Since all simulations created must all be put together in a single simulation, different Packet Tracer versions might raise some issues and, for that reason, every team member will be using the same version. In our case, it's going to be version 8.0.0.0212.

* Each VLAN has a unique name (starting with the VTP name - rcompddg5) and ID. 
We were given the VLAN ID range of 135 to 165.
More specifically, per building, we decided to place them the following way:
  - Building 1 -> 135 - 140;
  - Building 2 -> 141 - 145;
  - Building 3 -> 146 - 150;
  - Building 4 -> 151 - 155;
  
* The IPv4 network address of the backbone network: We were assigned an address space, which we had to divide in smaller blocks in order to split them for the diferent buildins.
This said, we divided our address block - 10.122.208.0/20 - in the following way:
  - Building 1 -> 10.122.208.0/23;
  - Building 2 -> 10.122.210.0/23;
  - Building 3 -> 10.122.212.0/23;
  - Building 4 -> 10.122.214.0/23;
  
* Instead of having only Address Range to cover the nodes requested, we decided to do some improvement and add to the subnet more nodes than necessary.
This is a way to make room for future upgrades to the network.
  
* With the gathering of the 4 buildings + Backbone, there will be only 1 switch with the VTP server role.
Until then, the building itself will have a switch called **Dummy_Connection** with the VTP server role.
  
* All devices should follow the specific name strategy - Building-Localization and other information-Device (ex: B2-Floor0-AP2) - or something similar;
  
* Connecting the devices, we decided to have some liberty regarding the specific type of cable used, since it was decided in the sprint before.
With that, we decided to choose the following cable strategy:
  - Between Switches: Fiber (FFE or FGE entrances);
  - Switches to Access Points: Fiber (FFE entrances);
  - Router to Switches: Fiber (FFE or FGE entrances);
  - Switches to PC: Copper (CFE entrances);
  - Switches to Servers: Fibber/Copper (FFE or CFE entrances);
  
* Our team was assigned with 120.57.210.186/30 as the ISP router IPv4 node address.

* Except for the VoIP phones, all other end devices are required to have a static and manually defined IPv4 configuration, including the default gateway.

* The default VLAN, with 1 as the ID, is going to be used to connect to the backbone.

# 3. Subtasks assignment #

* 1191513 - (T.2.1) Development of a layer two and layer three Packet Tracer
  simulation for building 1, and also encompassing the campus
  backbone. Integration of every members' Packet Tracer simulations into
  a single simulation.

* 1190743 - (T.2.2) Development of a layer two and layer three Packet Tracer
  simulation for building 2, and also encompassing the campus
  backbone.

* 1182147 - (T.2.3) Development of a layer two and layer three Packet Tracer
  simulation for building 3, and also encompassing the campus
  backbone.

* 1170640 - (T.2.4) Development of a layer two and layer three Packet Tracer
  simulation for building 4, and also encompassing the campus
  backbone.






