# Phase 1: Initial Lab Design

## Objective

The goal of Phase 1 is to design and prepare an isolated homelab network that is fully separated from the home network and suitable for practicing networking, systems administration, automation, and security.

## Design Principles

- Full isolation from the home network using dedicated firewall hardware
- Use of VLANs for internal segmentation
- Clear separation of management, server, client, and test networks
- Use of real enterprise-style switching hardware
- Security-first mindset: assume misconfiguration and plan for containment

## Hardware Overview

- Cisco Catalyst 2960-X (core switch)
- Cisco SG110-24HP (access switch)
- Approximately 8 x DDR3-based machines
- Dedicated firewall(s) (to be deployed)

## Network Segmentation Plan

- VLAN 10: Management
- VLAN 20: Servers
- VLAN 30: Clients
- VLAN 40: Test/Lab

Trunk links will be used between the core and access switch. Access ports will be assigned based on system role.

## Planned Roles

- Management / Automation Server (Ansible controller)
- Services Server (infrastructure services, logging, etc.)
- Security / Logging Server
- Client systems for testing
- Additional nodes reserved for future expansion and experiments

## Security Boundaries

- The lab will not be directly connected to the home network
- All lab traffic will pass through a dedicated firewall
- No services will be exposed to the internet
- Configuration examples committed to this repository will be sanitized

## Current Status

- Hardware staged but not yet interconnected
- Network design documented
- Firewall hardware selection and deployment pending

## Next Steps

- Deploy dedicated firewall hardware
- Configure core and access switching
- Implement VLAN segmentation
- Bring up initial Linux servers
- Begin Ansible-based configuration management
