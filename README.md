
# Azure Network Security & Secure Storage Administration Lab

## Project Overview

This project demonstrates hands-on experience configuring Microsoft Azure networking, network security, secure cloud storage, and Role-Based Access Control (RBAC).

The objective was to build a basic company-style cloud environment with restricted network access and secure document storage while applying cloud security best practices.

## Technologies Used

- Microsoft Azure
- Azure Virtual Network (VNet)
- Network Security Groups (NSG)
- Azure Blob Storage
- Azure Role-Based Access Control (RBAC)
- Microsoft Azure Portal

## Architecture

The project uses an Azure Virtual Network with a dedicated subnet and Network Security Group. An Azure Storage Account provides private document storage with restricted network access.

## Azure Resources

| Resource | Configuration |
|---|---|
| Resource Group | resource-group1 |
| Virtual Network | vnet-company |
| Region | East US 2 |
| Address Space | 10.0.0.0/16 |
| Subnet | snet-servers |
| Subnet Address | 10.0.1.0/24 |
| Network Security Group | nsg-server-security |
| Storage Account | stcloudlab707 |
| Blob Container | company-documents |

## Network Security Configuration

Created a Network Security Group to control inbound network traffic.

### Inbound Security Rule

| Setting | Configuration |
|---|---|
| Rule Name | Allow-RDP-MyIP |
| Port | 3389 |
| Protocol | TCP |
| Action | Allow |
| Priority | 300 |
| Source | Authorized public IP (/32) |

The NSG was associated with the `snet-servers` subnet.

The inbound rule restricts RDP traffic to an authorized IP address instead of allowing access from all sources.

## Storage Security Configuration

Created an Azure Storage Account with the following settings:

- Performance: Standard
- Redundancy: Locally Redundant Storage (LRS)
- Secure transfer required: Enabled
- Minimum TLS version: 1.2
- Anonymous blob access: Disabled
- Public network access: Enabled for selected networks and IP addresses

### Blob Storage

Created a private Blob container:

`company-documents`

Sample files uploaded:

- `company-policy.txt`
- `access-test.txt`

The container uses private access to prevent anonymous access to stored documents.

## Role-Based Access Control (RBAC)

Assigned the following built-in Azure role:

**Storage Blob Data Contributor**

This role allows the assigned user to:

- Read blob data
- Upload and modify blobs
- Delete blob data

The role was assigned at the Storage Account scope to demonstrate data-plane access management.

## Testing and Validation

The following tests are included in the project:

- [ ] Upload a blob
- [ ] Download a blob
- [ ] View blob properties
- [ ] Verify private container access
- [ ] Confirm authorized network access

Testing results will be documented after each test is completed.

## Project Screenshots

Screenshots documenting the project are stored in the `screenshots` folder.

| Screenshot | Description |
|---|---|
| 01 | Resource Group |
| 02 | Virtual Network Overview |
| 03 | Virtual Network Subnets |
| 04 | Network Security Group |
| 05 | NSG Subnet Association |
| 06 | NSG Inbound Rules |
| 07 | Storage Account Overview |
| 08 | Storage Networking Configuration |
| 09 | Blob Storage Access Testing |

## Skills Demonstrated

- Azure resource administration
- Virtual network configuration
- Subnet management
- Network Security Group configuration
- Inbound traffic filtering
- Azure Blob Storage administration
- Storage network restrictions
- Role-Based Access Control (RBAC)
- Cloud security fundamentals
- Technical documentation

## Project Goal

This project was developed as part of my preparation for the Microsoft Azure Administrator (AZ-104) certification.

It provides practical experience with Azure networking, storage administration, access control, and cloud security concepts relevant to entry-level IT support, networking, and cloud administration roles.



