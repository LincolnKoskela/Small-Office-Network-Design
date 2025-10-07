# Northside Security - Small Office Network Design Summary

## Objective
Design a secure and scalable small-office LAN for approximately 10 employees at Northside Security LLC.

## Topology Overview
Internet → Router (ISP) → Firewall → Managed Switch → Workstations, Wi-Fi Access Point, NAS, and Printer.

The firewall handles VLAN segmentation and routing between networks:
- VLAN 10 – Staff (192.168.10.0/24)
- VLAN 20 – Guest (192.168.20.0/24)
- VLAN 30 – Servers/Peripherals (192.168.30.0/24)

## Security Policies
- Guest VLAN isolated from all internal VLANs (internet-only access).  
- Staff VLAN permitted limited access to Servers VLAN (NAS/Printer).  
- Management VLAN accessible only to IT admins for device management.  
- All outbound traffic filtered through the firewall.

## Hardware Components
| Device | Role |
|--------|------|
| Firewall | VLAN routing and security filtering |
| Managed Switch | VLAN tagging and trunking |
| Access Point | SSIDs mapped to VLAN 10 (Staff) and VLAN 20 (Guest) |
| NAS | Centralized file storage and local backup |
| Printer | Shared resource in Servers VLAN |

## Future Enhancements
- Add site-to-site VPN for remote access  
- Implement endpoint security on client PCs  
- Deploy automated cloud backup integration
