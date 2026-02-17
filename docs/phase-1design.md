# Phase 1: Initial Lab Design 

## Objective
The goal of phase one is to design and prepare an isolated homelab network that is fully seperated from the home network and is sutiable for practicing networking, system administration , automation , and security.(

## Design Principles 
- Full isolation from the home network using dedicated firewall hardware
- Use of VLANS for internal segmentation
- Clear seperation of management, server, client, and test networks
- Use of real enterprise-style switching hardware (Cisco)
- Security first mindset: assume misconfiguration and plan for containment

## Hardware Overview
- Cisco Catalyst 2960-X (core switch)
- Cisco SG110-24HP (access switch)
- Approxmately 8 x DDR3-based machines
- Dedicated firewalls (to be deployed)

## Network Segmentaion Plan
- VLAN 10: Mangement
- VLAN 20: Servers
- VLAN 30: Clients
- VLAN 40: Test/Lab

Trunk links will be used between the core and access switch. Access ports will be assigned based on system role.

## 
