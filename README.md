# Azure Virtual Network Lab

## Project Overview

## Objectives

## Azure Services Used

## Step 1 – Create a Virtual Network

## Step 2 – Create a Resource Group

## Step 3 – Create Subnet11

## Step 4 – Create a Network Security Group (NSG)

## Project Summary

## Skills Demonstrated

## Lessons Learned


## References# 


Azure-Virtual-Network-Lab

Deploying and configuring an Azure Virtual Network with subnets and network security in Microsoft Azure.

## Project Overview

This project demonstrates how I deployed and configured an Azure Virtual Network (VNet) in Microsoft Azure. The project includes creating a Resource Group, configuring a Virtual Network, creating subnets, and securing the network with a Network Security Group (NSG).

## Objectives

- Create a Resource Group
- Create a Virtual Network
- Configure an Address Space
- Create Subnets
- Secure the network using a Network Security Group (NSG)

## Azure Services Used

## Step 1 – Create a Network Security Group (NSG)

### Purpose

A Network Security Group (NSG) is an Azure networking service that controls inbound and outbound network traffic using security rules. It acts as a virtual firewall to help protect Azure resources from unauthorized access.

### Configuration

| Setting | Value |
|---------|-------|
| Network Security Group | Olorode-NSG |
| Resource Group | Goodnews |
| Region | East US |

### Why This Is Important

Network Security Groups provide an additional layer of security by filtering network traffic based on rules. This helps ensure that only authorized traffic can reach resources deployed within the Virtual Network.

### Screenshot

![Network Security Group Overview](screenshots/05-network-security-group-overview.png)

## Key Learning

During this step, I created a Network Security Group (NSG) to secure my Azure network. I learned that NSGs use inbound and outbound security rules to control which traffic is allowed or denied, helping protect Azure resources from unauthorized access.

## AZ-104 Skills Covered

- Azure Network Security Groups
- Network Security
- Traffic Filtering
- Azure Networking

## Interview Question

**Question:** What is a Network Security Group (NSG) in Azure?

**Answer:** A Network Security Group (NSG) is an Azure networking service that controls inbound and outbound traffic using security rules. It can be associated with a subnet or a network interface to protect Azure resources by allowing or denying specific types of network traffic.


## Real-World Use Case

In a production environment, Network Security Groups are commonly used to restrict access to Azure resources. For example, a company might allow HTTP (port 80) and HTTPS (port 443) traffic to a web server while blocking all other inbound connections to reduce the attack surface.


## Step 2 – Create a Resource Group

### Purpose

A Resource Group is a logical container in Microsoft Azure that holds related resources for a project. It makes it easier to deploy, manage, monitor, and delete resources together.

### Configuration

| Setting | Value |
|---------|-------|
| Resource Group Name | Goodnews |
| Region | East US |

### Why This Is Important

Using a Resource Group allows all resources for this networking project to be managed as a single unit. This simplifies administration and helps with cost management and organization.

### Screenshot

![Resource Group Overview](screenshots/02-resource-group-overview.png)


## Interview Question

**Question:** What is a Resource Group in Azure?

**Answer:** A Resource Group is a logical container that groups related Azure resources together. It helps organize, manage, monitor, and control access to resources within a project.
![Virtual Network Overview](screenshots/01-vnet-overview.png)
- Azure Network Security Groups



## Step 3 – Create Subnet11

### Purpose

A subnet divides a Virtual Network into smaller network segments. This improves network organization, enhances security, and allows resources to be grouped based on their function.

### Subnet Configuration

| Setting | Value |
|---------|-------|
| Subnet Name | Subnet11 |
| Address Range | 10.0.1.0/24 |

### Why This Is Important

Creating a dedicated subnet allows Azure resources to be logically separated within the Virtual Network. This makes it easier to apply security controls, manage network traffic, and isolate workloads as the environment grows.

### Screenshot

![Subnet11 Configuration](screenshots/03-subnet11-configuration.png)

## Key Learning

In this step, I learned how to create and configure subnets within an Azure Virtual Network. Subnets help organize resources, reduce unnecessary network traffic, and provide better security by separating workloads into different network segments.

## AZ-104 Skills Covered

- Azure Virtual Networks
- Azure Subnets
- IP Address Planning
- Network Segmentation

- ## Interview Question

**Question:** What is the purpose of a subnet in Azure?

**Answer:** A subnet is a smaller network within a Virtual Network. It allows Azure resources to be organized into separate network segments, improving security, performance, and management.


## Step 4 – Review Inbound Security Rules

### Purpose

Inbound security rules control the traffic that is allowed to enter Azure resources. These rules help protect resources by permitting only approved network connections.

### Default Inbound Rules

Azure automatically creates several default inbound rules for every Network Security Group.

| Priority | Rule | Action |
|----------|------|--------|
| 65000 | AllowVNetInBound | Allow |
| 65001 | AllowAzureLoadBalancerInBound | Allow |
| 65500 | DenyAllInBound | Deny |

### Why This Is Important

These default rules provide a secure baseline. Additional custom rules can be added to allow services such as HTTP, HTTPS, RDP, or SSH when required.

### Screenshot

![Inbound Security Rules](screenshots/07-inbound-security-rules.png)

## Key Learning

During this step, I learned that inbound security rules determine which incoming network traffic is allowed or denied. Azure automatically applies default rules, but administrators can create custom rules to meet specific application and security requirements.

## Real-World Use Case

A company hosting a public website may create an inbound rule to allow HTTP (port 80) and HTTPS (port 443) traffic while denying all other inbound connections. This helps reduce the attack surface and protects the application from unauthorized access.

## AZ-104 Skills Covered

- Azure Network Security Groups
- Inbound Security Rules
- Network Traffic Filtering
- Azure Networking Security
- 
