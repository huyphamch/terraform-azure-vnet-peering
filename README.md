## Description
1. The Rand Enterprises Corporation is evaluating Azure as a deployment platform. To help the company with its evaluation, you need to create virtual networks in the region specified by Rand Enterprises Corporation. You have to create test virtual machines in two virtual networks, establish connectivity between the two networks via VNet peering, and ensure connectivity is established properly.
<br />
To test the platform, Rand Enterprises Corporation wants to onboard an employee on the company’s default Azure Active Directory and assign a Custom RBAC role, under which they will be able to read the network and storage along with the VM. Under this custom RBAC, the employee should also be given permission to start and restart the VM. You have to onboard the employee under the default Azure AD and create a custom RBAC for the role of computer operator for this employee.
<br />
As a security measure, you need to ensure that the onboarded user can only access the resources mentioned in the custom role and adhere to the principle of least privilege.

2. The Rand Enterprises Corporation wants to deploy a web application in a highly available environment so that only the healthy instances will be serving the traffic so end users will not be facing any downtime. They have decided to work on an Azure public load balancer to implement the functionality.

The operations team at Rand decides to define the entire architecture using the load balancer and its backend pool, once that’s in place they intend to create the frontend IP and health probe along with virtual machines housing their application.
<br />
Rand Enterprises works extensively on delivering highly available web applications for their users in a secure way by avoiding directly exposing the virtual machines hosting the applications to the public internet. The communication from the application in the VM to the end-user must take place via the Load Balancer.
<br />
The expectation of the operation team is to create a reusable method that can be used for automation if in the future we need to deploy the same kind of infrastructure. So, rather than deploying resources in the Azure portal, they should leverage the command-line interface to deploy the resources so that in the future these commands can be used
<br />
As a security measure, you need to ensure that only the health instances of the virtual machine will be serving the traffic.

## Objectives
1. To connect Internet workloads using Vnet peering and assign a custom role for operating these workloads.
Expected Deliverables:
- Identify the networks
- Workload deployed to these networks
- Establishing the connectivity between these networks
- Onboard a user
- Create and assign a custom role to the user.

2. To create high available architecture by distributing incoming traffic among healthy service instances in cloud services or virtual machines in a load-balanced set with the help of a command-line interface
Expected Deliverables:
- Identify Virtual machines and Networking
- Configure the load balancer
- Extend the load balancer with backend pool and frontend IP
- Define the Health probe

## Usage
<br /> 1. Open terminal
<br /> 2. Before you can execute the terraform script, your need to configure your Azure environment first.
<br /> az login --user <myAlias@myCompany.onmicrosoft.com> --password <myPassword>
<br /> Update tenant_id in variables.tf (az account tenant list)
<br /> Update subscription_id in variables.tf (az account subscription list)
<br /> Update custom_email in variables.tf (az account show)
<br /> 3. Now you can apply the terraform changes.
<br /> terraform init
<br /> terraform apply --auto-approve
<br /> 4. tbd.
<br /> Test result: Ping answer messages received.
<br /> 5. At the end you can cleanup the created AWS resources.
<br /> terraform destroy --auto-approve
