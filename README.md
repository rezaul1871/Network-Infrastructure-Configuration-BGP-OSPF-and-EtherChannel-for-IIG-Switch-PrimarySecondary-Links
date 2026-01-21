# Network-Infrastructure-Configuration-BGP-OSPF-and-EtherChannel-for-IIG-Switch-PrimarySecondary-Links
**EtherChannel Modes: PAgP (desirable/auto - Cisco), LACP (active/passive - standard), and static (on). Choose LACP active for multi-vendor compatibility, PAgP desirable for Cisco-only, or static for simple setups. Each port-channel group must use one consistent protocol with matching modes on both sides for proper formation and redundancy.**


**Network Infrastructure Configuration for High Availability**
**Core Components:**

**EtherChannel Configuration:**
- Implementation of port aggregation using either PAgP (Cisco proprietary) or LACP (IEEE standard) protocols
- Primary and secondary EtherChannel groups with distinct path prioritization
- Protocol mode selection guidance: active/desirable for initiating negotiation, passive/auto for responding

**OSPF Routing Configuration:**
- OSPF cost manipulation to establish primary and secondary path preferences
- Area design for optimal convergence and scalability
- Passive interface configuration for security optimization

**BGP Routing Configuration:**
- BGP configuration 
- Path preference control using local preference and AS path.

**Path Selection Strategy:**
- BGP as Primary path and secondary as OSPF.
- If BGP path down,it will trun on is OSPF path

**Verification and Troubleshooting:**
- Reachable with each end node
- Tracerouter to find path after primary path down.

  ![alt text](https://github.com/rezaul1871/Network-Infrastructure-Configuration-BGP-OSPF-and-EtherChannel-for-IIG-Switch-PrimarySecondary-Links/blob/071d1bdbec99ae133c3e056bf8331f1d4d8586d9/Topology.png)

This configuration framework ensures network resilience through multiple layers of redundancy, with automatic failover during link or device failures while maintaining optimal path selection during normal operations. The design principles emphasize standardization, multi-vendor compatibility where applicable, and maintainability through consistent configuration patterns.
