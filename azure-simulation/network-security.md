
# Azure Network Security Lab

## Objective
Design a basic Azure network for a company
hosting a Windows file server.

## Network Design

Resource Group: rg-pilot-fileserver

Virtual Network: vnet-pilot

Address Space: 10.0.0.0/16

Subnet: web

Subnet Address Range: 10.0.1.0/24

Virtual Machine: vm-fs01

Operating System: Windows Server 2022

## Network Security

A Network Security Group (NSG) controls
inbound and outbound network traffic.

Security considerations:

- Restrict Remote Desktop access.
- Avoid unrestricted inbound traffic.
- Allow only necessary network connections.
- Review inbound and outbound rules.
- Avoid exposing management services publicly.

## Questions

1. What is the purpose of a VNet?
2. Why do we use subnets?
3. What does an NSG protect?
4. Why should RDP access be restricted?
5. What is the difference between a
   Resource Group and a Virtual Network?

## Lab Environment

Azure configuration was practiced using
a simulator.

No actual Azure resources were deployed.

## Lessons Learned

(Add your answers after completing the lab.)
