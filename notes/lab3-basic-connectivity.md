# Lab 3 -- TCP/IP Model and Basic Connectivity (Day 3)

**Objective**: Configure basic IP addresses and verify connectivity layer by layer.

**Topology:**

```
PC1 ── Fa0/1 ── SW1 ── Fa0/2 ── R1 (Gi0/0)
PC2 ── Fa0/3 ── SW1

IP Addressing:
PC1   → 192.168.1.10 / 255.255.255.0 / GW: 192.168.1.1
PC2   → 192.168.1.11 / 255.255.255.0 / GW: 192.168.1.1
R1 Gi0/0 → 192.168.1.1 / 255.255.255.0
```

## Tasks
Step 1 -- Configure PC1 IP address
Click PC1 → Desktop → IP Configuration
→ IP: 192.168.1.10
→ Subnet: 255.255.255.0
→ Gateway: 192.168.1.1
(repeat for PC2 with .11)

Step 2 -- Configure R1 interface
Click R1 → CLI tab → type:
R1> enable
R1# configure terminal
R1(config)# interface GigabitEthernet0/0
R1(config-if)# ip address 192.168.1.1 255.255.255.0
R1(config-if)# no shutdown
R1(config-if)# end

Step 3 -- Verify Layer 1 (Physical)
R1# show interfaces GigabitEthernet0/0
→ Line 1: "GigabitEthernet0/0 is up, line protocol is up"
→ Both must say "up" ✅
→ "up / down" = Layer 1 fine, Layer 2 problem
→ "down / down" = physical cable problem

Step 4 -- Verify Layer 2 (Data Link)
R1# show interfaces GigabitEthernet0/0
→ Look for: "Hardware is..." and MAC address line

Step 5 -- Verify Layer 3 (Network)
R1# show ip interface brief
→ GigabitEthernet0/0 should show:
  192.168.1.1   YES   manual   up   up

Step 6 -- Test end-to-end connectivity
Click PC1 → Desktop → Command Prompt
PC1> ping 192.168.1.11    ← PC1 to PC2
PC1> ping 192.168.1.1     ← PC1 to router

→ 5 pings should return:
  "Reply from 192.168.1.1: bytes=32 time=..."
→ First ping may fail (ARP resolution) -- that's normal ✅