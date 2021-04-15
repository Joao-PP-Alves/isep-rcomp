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
  Building 1 -> 135 - 140;
  Building 2 -> 141 - 145;
  Building 3 -> 146 - 150;
  Building 4 -> 151 - 155;
  
* The IPv4 network address of the backbone network: We were assigned an address space, which we had to divide in smaller blocks in order to split them for the diferent buildins.
This said, we divided our address block - 10.122.208.0/20 - in the following way:
  Building 1 -> 10.122.208.0/23;
  Building 2 -> 10.122.210.0/23;
  Building 3 -> 10.122.212.0/23;
  Building 4 -> 10.122.214.0/23;
  
* With the gathering of the 4 buildings + Backbone, there will be only 1 switch with the VTP server role.
Until then, the building itself will have a switch called **Dummy_Connection** with the VTP server role.
  
* Our team was assigned with 120.57.210.186/30 as the ISP router IPv4 node address.


# 3. Subtasks assignment #

* 1191513 - (T.2.1) Development of a layer two and layer three Packet Tracer
  simulation for building A, and also encompassing the campus
  backbone. Integration of every members' Packet Tracer simulations into
  a single simulation.

* 1190743 - (T.2.2) Development of a layer two and layer three Packet Tracer
  simulation for building B, and also encompassing the campus
  backbone.

* 1182147 - (T.2.3) Development of a layer two and layer three Packet Tracer
  simulation for building C, and also encompassing the campus
  backbone.

* 1170640 - (T.2.4) Development of a layer two and layer three Packet Tracer
  simulation for building D, and also encompassing the campus
  backbone.






