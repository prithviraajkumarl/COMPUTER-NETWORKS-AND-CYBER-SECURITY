ECA6101CO4AT3_REPORT

Name: Prithvi Raaj Kumar L
Registration Number: 4357 / 192512275
Department: Electronics and Communication Engineering (ECE)

Implementation and Evaluation of a 3-Branch Site-to-Site VPN
1. Architecture Design
The objective of this assessment was to design and implement a site-to-site VPN architecture connecting three geographically separated branch offices. A full-mesh WAN topology was created using Cisco Packet Tracer.

Hardware Components:

3 × Cisco 2911 Routers (R1, R2, R3)

3 × Cisco 2960-24TT Switches

End-user PCs for each branch LAN

IP Addressing Scheme:

Branch 1 LAN: 192.168.1.0/24 (Gateway: 192.168.1.1)

Branch 2 LAN: 192.168.2.0/24 (Gateway: 192.168.2.1)

Branch 3 LAN: 192.168.3.0/24 (Gateway: 192.168.3.1)

WAN Transit Links (Serial/Gigabit): 10.0.12.0/30, 10.0.13.0/30, 10.0.23.0/30

VPN Tunnel Links: 172.16.12.0/30, 172.16.13.0/30, 172.16.23.0/30

Network Topology Reference Diagram:
[Insert image_0b4fe4.jpg here]

Implementation Screenshot:
[Insert image_0b501a.png here]

2. VPN Implementation Details
To enable dynamic routing across the geographically separated networks, OSPF (Open Shortest Path First) was configured on all three routers.

To establish the site-to-site VPN, GRE (Generic Routing Encapsulation) Tunnels were configured between the branch routers. This creates a logical overlay network, allowing the branch LANs to communicate securely across the simulated public transit network. Tunnel interfaces (Tunnel12, Tunnel13, and Tunnel23) were successfully brought up and mapped to their respective physical transit interfaces.

3. Evaluation of Connectivity
Result: Highly Successful

Inter-branch connectivity was verified using ICMP (ping) requests from the end devices in each LAN. Testing confirmed that PC1 (Branch 1) could successfully reach both PC2 (Branch 2) and PC3 (Branch 3). The successful transmission of packets proves that the GRE tunnels are actively encapsulating and routing LAN traffic across the WAN. The underlying OSPF configuration accurately mapped the network routes through the tunnel interfaces.

4. Evaluation of Reliability
Result: Highly Reliable

The network demonstrated excellent reliability, showing 0% packet loss during sustained ICMP testing after the initial ARP resolution and tunnel establishment phases. Furthermore, because a full-mesh tunnel design was implemented (R1 to R2, R1 to R3, R2 to R3), the architecture inherently supports routing redundancy. In the event of a single WAN link failure, OSPF will dynamically recalculate the path and reroute traffic through the surviving branch tunnel, preventing a complete loss of inter-branch communication.

5. Evaluation of Confidentiality
Result: Limited (Encapsulated but Unencrypted)

The current architecture successfully utilizes GRE tunneling to encapsulate private LAN traffic over the simulated public transit network, creating a private virtual connection. However, due to IOS feature limitations within the specific Cisco 2911 Packet Tracer image utilized for this simulation (Version 15.1(4)M4), the IPsec (ISAKMP/Crypto) command sets were unavailable.

Because GRE does not natively provide cryptographic encryption (such as AES) or hashing (such as SHA), the data payload within the tunnels technically remains in plaintext. While the traffic is isolated from the underlying routing table of the transit network, true military-grade confidentiality is not achieved. In a real-world, production deployment, this architecture must be upgraded to IPsec over GRE or a pure IPsec Site-to-Site VPN to ensure that intercepted data cannot be read by unauthorized third parties.
