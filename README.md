# Homelab Network

This repository documents the design and build of my isolated homelab network using real hardware. The lab is fully segregated from my home network and is designed for practicing networking, systems administration, automation, and security.

## Goals

- Build a segmented lab network using Cisco switching
- Keep the lab isolated behind dedicated firewalls
- Practice real-world network design and troubleshooting
- Provide a platform for Ansible automation and Linux hardening projects
- Document the full build process and design decisions

## Hardware

- Cisco Catalyst 2960-X (core switch)
- Cisco SG110-24HP (access switch)
- ~8 x DDR3-based machines (mixed roles)
- Dedicated firewall(s) (planned)

## Planned Architecture

- The lab will be isolated from the home network using a dedicated firewall
- VLAN-based segmentation:
  - VLAN 10 - Management
  - VLAN 20 - Servers
  - VLAN 30 - Clients
  - VLAN 40 - Test/Lab
- Trunk link between the Catalyst 2960-X and SG110-24HP
- Access ports assigned per role

## Planned Roles

- Management / Automation Server (Ansible controller)
- Services Server (infrastructure services, logging, etc.)
- Security / Logging Server
- Client systems for testing
- Additional nodes for future expansion

## Security Model

- Physical and logical separation from the home network
- Firewall-enforced segmentation at the lab edge
- No direct exposure to the internet
- Internal segmentation using VLANs and access controls

## Current Status

Phase 1: Design and preparation (in progress)  
- Hardware staged but not yet connected  
- Network design and documentation in progress  

## Future Work

- Deploy firewall and core switching
- Implement VLANs and trunking
- Bring up initial servers and clients
- Integrate Ansible for configuration management
- Add logging and monitoring
- Document configurations and lessons learned
