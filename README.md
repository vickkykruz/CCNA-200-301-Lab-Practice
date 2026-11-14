# CCNA 200-301 Lab Practice

## About This Repository

Hands-on Cisco Packet Tracer labs built alongside **Jeremy's IT Lab** (*Acing the CCNA Exam, Volume 1* by Jeremy McDowell) and the Cisco 200-301 exam blueprint.

The goal is exam-ready confidence through deep command knowledge and practical lab work. Each lab maps to a specific study day and reinforces the CLI skills needed for the real exam.

## Labs Completed

| Lab | Topic | Key Skills | Status |
| --- | --- | --- | --- |
| Lab 1 | Network Devices | Device types, topology building, cable selection | ✅ Done |
| Lab 2 | Cables and Interfaces | Straight-through/crossover, serial (HWIC-2T), SFP fibre modules | ✅ Done |
| Lab 3 | Basic IP Connectivity | IPv4 addressing, `no shutdown`, `show interfaces`, ping | ✅ Done |
| Lab 4 | Full Network Build | Multi-device topology, default gateway, end-to-end connectivity | ✅ Done |

## Tools Used

- **Cisco Packet Tracer 8.x** — topology simulation
- **Jeremy's IT Lab** — *Acing the CCNA Exam, Volume 1* (Jeremy McDowell, Manning Publications)
- **Cisco IOS CLI** — router and switch command practice
- **Boson ExSim-Max** — exam-style practice questions

## Topics Covered

**Day 1 — Network Devices (Ch. 2)** Device types (router, switch, firewall, AP), topology building, cable selection rules

**Day 2 — Interfaces and Cables (Ch. 3)** Straight-through vs crossover cables, serial ports (HWIC-2T module), SFP fibre (GLC-SX-MMD for MMF, GLC-LH-SMD for SMF), link status indicators

**Day 3 — Basic IPv4 Connectivity (Ch. 7–8)** IPv4 addressing, subnet masks, default gateway, `no shutdown` on router interfaces, `show interfaces`, `show ip interface brief`, end-to-end ping testing

## How to Use These Files

1. Open the `.pkt` file in Cisco Packet Tracer 8.x
2. Read the matching notes in `/notes/` for key commands and concepts
3. Try to recreate the topology from scratch before looking at the solution
4. Use `show` commands to verify every interface — don't just ping and move on

## Repo Structure

```
ccna-200-301-lab-practice/
├── README.md
├── labs/
│   ├── lab1-network-devices.pkt
│   ├── lab2-cables-interfaces.pkt
│   ├── lab3-basic-connectivity.pkt
│   └── lab4-full-network.pkt
├── screenshots/
└── notes/
    ├── etherchannel-commands.md
    └── stp-commands.md
```
