# Implement and Manage Virtual Networking

## Overview

I created an additional subnet and a separate branch virtual network. Then i configured bidirectional VNet peering, network security groups, static private and public IP addresses, route tables and user defined routes. I also configured a Microsoft.Storage service endpoint and created a private DNS zone with a virtual network link.

At the end i deployed a Standard Azure Load Balancer with a frontend IP configuration, backend pool, TCP health probe and HTTP load-balancing rule. also enabled Azure Network Watcher in East Asia. Verified the deployed configurations using the Azure Portal, Azure CLI and PowerShell.

---

## Screenshots

### Additional Subnet Configuration

Shows the creation of an additional subnet in the existing virtual network.

![Additional Subnet Configuration](screenshots/01-azure-vnet-additional-subnet-configuration.png)

### Subnet CLI and PowerShell Verification

Shows the subnet address ranges retrieved and verified using Azure CLI and PowerShell.

![Subnet Verification](screenshots/02-azure-vnet-subnet-cli-powershell-verification.png)

### Branch Network Deployment

Shows the deployment of the branch virtual network and its subnet.

![Branch Network Deployment](screenshots/03-azure-vnet-branch-network-deployment.png)

### Bidirectional VNet Peering

Shows the peering configuration connecting the main virtual network and the branch virtual network.

![Bidirectional VNet Peering](screenshots/04-azure-vnet-bidirectional-peering-configuration.png)

### Network Security Group Rules

Shows the custom inbound security rules configured on `nsg-branch-1`, including the RDP deny and HTTPS allow rules.

![NSG Inbound Rules](screenshots/05-azure-vnet-branch1-custom-nsg-inbound-security-rules.png)

### Static Private IP Configuration

Shows the static private IP address `10.20.1.10` assigned to the branch network interface.

![Static Private IP](screenshots/06-azure-vnet-static-private-ip-configuration.png)

### Public IP Configuration

Shows the Standard public IP address created for the branch networking environment.

![Public IP Configuration](screenshots/07-azure-vnet-public-ip-configuration.png)

### Private IP CLI and PowerShell Verification

Shows the network interface configuration and verification of its static private IP address using Azure CLI and PowerShell.

![Private IP Verification](screenshots/08-azure-vnet-static-private-ip-cli-powershell-verification.png)

### User-Defined Route Configuration

Shows the custom route configured to block traffic destined for `192.0.2.0/24`.

![UDR Configuration](screenshots/09-azure-vnet-udr-route-configuration.png)

### Route Table Deployment

Shows the deployed route table `rt-branch-1` and its configuration.

![Route Table Deployment](screenshots/10-azure-vnet-route-table-deployment.png)

### Route Table Subnet Association

Shows the association of the route table with `snet-branch-1`.

![Route Table Association](screenshots/11-azure-vnet-udr-subnet-association.png)

### Storage Service Endpoint Configuration

Shows the Microsoft.Storage service endpoint selected for the branch subnet.

![Storage Service Endpoint](screenshots/12-azure-vnet-storage-service-endpoint-configuration.png)

### Private DNS Zone and VNet Link

Shows the private DNS zone `lab.inno.internal` and its virtual network link.

![Private DNS Zone](screenshots/13-azure-vnet-private-dns-zone-and-vnet-link.png)

### Azure Load Balancer Configuration

Shows the deployed Standard Load Balancer `lb-branch-1`, its frontend public IP, backend pool and configured health probe and load-balancing rule.

![Load Balancer Configuration](screenshots/14-azure-vnet-load-balancer-configuration.png)

### Load Balancer Health Probe and Rule

Shows the TCP health probe and HTTP port 80 load-balancing rule configured on the Load Balancer.

![Load Balancer Probe and Rule](screenshots/15-azure-vnet-load-balancer-probe-and-rule.png)

### Azure Network Watcher

Shows the enabled Network Watcher resource in the East Asia region.

![Network Watcher](screenshots/16-azure-vnet-network-watcher-diagnostic.png)