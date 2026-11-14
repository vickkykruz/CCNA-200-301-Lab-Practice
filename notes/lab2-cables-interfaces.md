# Lab 2 -- Cables and Interfaces (Day 2)

**Objective**: Correctly cable a network and identify interface types.

**Topology:**

```
PC1 ──────── SW1 ──────── R1
PC2 ──────────┘
                          │
                         R2
```

## Tasks:

1. Connect all devices using correct cable types
   (Packet Tracer will show amber/red if wrong)

2. Click on R1 → Physical tab
   → What interface type connects to SW1?
   → What speed does the interface show?

3. Click on SW1 → Physical tab
   → What type are the ports? (FastEthernet or GigabitEthernet?)
   → How many ports does a 2960 switch have?

4. Connect R1 to R2 using a SERIAL cable
   → Drag a serial DCE cable between them
   → R1 Serial0/0/0 → R2 Serial0/0/0
   → Click R1 → Config → Serial0/0/0
   → Tick the "Clock Rate" box (DCE end sets clock rate)
   → Set clock rate to 64000

5. Verify all links show GREEN
   → Amber = interface is up but STP converging
   → Red = physical problem or shutdown
   → Green = fully up ✅