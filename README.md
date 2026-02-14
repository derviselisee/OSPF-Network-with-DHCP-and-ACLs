# OSPF Network with DHCP and ACLs
Implementation of OSPF Network with DHCP and ACLs Configurations.


In this project, I designed and configured a fully functional enterprise-level network in Cisco Packet Tracer using 4 routers, multiple switches,
and end-user devices (PCs and servers). The main goal was to ensure full connectivity using OSPF as the dynamic routing protocol,
assign IP addresses dynamically with DHCP, and enforce access restrictions using extended ACLs

 What I Did ?

  1. Basic Router & Interface Configuration

-I started by assigning hostnames to each router to keep the topology organized.

-Configured IP addresses on all interfaces, including both the router interconnections and LAN segments.

-Set passwords for console and VTY lines to enhance security.

 2. DHCP Configuration on Each Router

-I configured each router as a DHCP server for its own subnet:

For example, Router A served the 192.168.10.0/24 network for PCs like MII and OCEANE.

Router B handled DHCP for 192.168.20.0/24, and so on.

All end devices received their IP addresses dynamically, proving that DHCP was working correctly.


 3. OSPF (Open Shortest Path First) Implementation

I enabled OSPF routing protocol on all routers and interfaces.

Configured a Loopback interface on each router to provide a stable and reliable !

Advertised all LAN and inter-router networks using the OSPF network command.

I then used Simulation Mode to verify that the entire network could route packets properly, ensuring all subnets could communicate.


4. ACLs (Access Control Lists)
   
I implemented extended ACLs to enforce traffic filtering between specific hosts. These are the rules I applied:

-Blocked GNON (192.168.20.2) from communicating with DERVIS (192.168.30.1)
-Blocked OCEANE (192.168.10.2) from communicating with GNON (192.168.20.2)
-Blocked MII (192.168.10.1) from accessing the File Server (192.168.40.2)

Each ACL used the access-list command to deny traffic from a specific source to a destination, then applied to the relevant router interface using ip access-group.

![Network Topology](https://github.com/user-attachments/assets/8901fb2c-85e6-47e0-bf10-13eacbcd7ee5)
![Instructions](https://github.com/user-attachments/assets/f51d1893-d9cc-45e7-8f0a-d2364571efb0)

![Router D OSPF Route](https://github.com/user-attachments/assets/2755c3f8-6d9b-4fb6-93de-f04f57f617f6)
![Router C OSPF Route](https://github.com/user-attachments/assets/23786965-8351-49d0-935f-09fcc4338af7)
![Router B OSPF Route](https://github.com/user-attachments/assets/19083226-cb2e-4ee1-b9ae-80d307f37ac1)
![Router A OSPF Route](https://github.com/user-attachments/assets/6b382dc8-b06b-4496-8e8c-e8f784f891f5)
![Dhcp Server Router D](https://github.com/user-attachments/assets/0b0ddd8e-3bbf-4aa2-b0e4-4e49918238d9)
![Dhcp Server Router C](https://github.com/user-attachments/assets/2d8ebac6-23aa-4945-a059-8fbc0e3f8040)
![Dhcp Server Router B](https://github.com/user-attachments/assets/61ec902b-b8b7-4248-8ae0-b5a1a1868d98)
![Dhcp  Server Router A](https://github.com/user-attachments/assets/12b3f938-8afa-448c-82be-881f7b271f39)
![ACLs Entries 2 and 3 ](https://github.com/user-attachments/assets/387639c2-93dc-4f8c-a3a8-af1dc24aae82)
![ACL Entry 1](https://github.com/user-attachments/assets/62066962-32fe-446b-905d-fc8291ffd0fe)


