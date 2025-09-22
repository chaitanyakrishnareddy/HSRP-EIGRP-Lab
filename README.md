HSRP-EIGRP-Lab# HSRP + EIGRP Redundancy Lab 

This lab demonstrates Hot Standby Router Protocol (HSRP) with Enhanced Interior Gateway Routing Protocol (EIGRP) 
for WAN redundancy. An ISP router advertises a loopback interface (8.8.8.8) as the simulated Internet.  

Features
- HSRP between two routers (R1 active, R2 standby)
- EIGRP for dynamic routing with ISP
- Loopback on ISP (8.8.8.8) as a test Internet address
- WAN link failure triggers HSRP failover

IP Addressing
- LAN: 192.168.1.0/24
- HSRP Virtual IP: 192.168.1.3
- R1 LAN: 192.168.1.1
- R2 LAN: 192.168.1.2
- ISP Loopback: 8.8.8.8/32
- WAN Links: 10.0.0.0/30 and 10.0.0.4/30

Verification
1. show standby brief → Check Active/Standby
2. show ip eigrp neighbors → Verify adjacency with ISP
3. ping 8.8.8.8 → Test Internet connectivity
4. Shut down R1 WAN → R2 becomes Active automatically
