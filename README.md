# Beginner-Friendly Home Lab for Learning Networking

This guide outlines a low-cost, practical home lab setup for early-career network engineers. It’s designed around used and off-the-shelf hardware, most of which can be sourced from eBay, Facebook Marketplace, or local IT recyclers.

## Goals

- Understand Layer 2/3 networking
- Practice VLANs, DHCP, DNS, and NAT
- Experiment with firewalls and VPNs
- Use virtualization for simulated labs
- Keep costs and power usage low

---

## Hardware List

| Component          | Model/Option                         | Est. Cost | Notes |
|-------------------|--------------------------------------|-----------|-------|
| **Router**         | TP-Link ER605                        | $55–$70   | VLAN & VPN capable, Omada ecosystem |
| **Switch**         | Cisco Catalyst 2960G / HP 1810G      | $30–$60   | Managed, supports VLANs and trunking |
| **Lab Server**     | Dell OptiPlex 7010/9010 or Lenovo M92p | $60–$100 | Run VMs, pfSense, GNS3, etc. |
| **Wi-Fi AP**       | Ubiquiti UniFi AC Lite / TP-Link EAP225 | $30–$50 | VLAN-capable wireless |
| **Cables**         | 10–20x CAT5e/6 patch cables           | ~$15      | Bulk packs are cheaper |
| **(Optional)** Rack & Patch Panel | 4U–12U open frame, wall mountable | $20–$40 | Optional but helpful |

**Total Budget:** ~$200–$250

---

## Example Topology
