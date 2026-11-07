# Azure Subscription Governance

## Overview

I demonstrated Azure subscription governance by inspecting subscription and resource-group details, assigning the built-in **Require a tag on resources** Azure Policy and verifying compliance.

I assigned the policy to `rg-rbac-lab` with the required tag `Environment = Lab` and the **Deny** effect. I deployed an Ubuntu virtual machine and applied the tag to its associated resources. I confimed all seven evaluated resources were compliant using Azure Portal and PowerShell. 

---

## Screenshots

### Subscription Overview

Shows Azure CLI login and the active subscription.

![Subscription Overview](screenshots/01-azure-sub-cli-login-subscription-overview.png)

### Subscription Queries

Shows subscription details in JSON format and a JMESPath query.

![Subscription Queries](screenshots/02-azure-sub-subscription-json-and-cli-queries.png)

### Resource Group Governance

Shows subscription and resource-group inspection, including the management-group permission limitation.

![Resource Group Governance](screenshots/03-azure-subscription-and-resource-group-governance.png)

### VM Deployment

Shows the successful deployment of the Ubuntu virtual machine.

![VM Deployment](screenshots/04-azure-sub-policy-vm-deployment-success.png)

### VM Running

Shows the deployed VM in the Running state.

![VM Running](screenshots/05-azure-sub-policy-vm-running-overview.png)

### Azure Policy Compliance Dashboard

Shows overall subscription compliance and the separate ASC Default initiative findings.

![Azure Policy Compliance Dashboard](screenshots/06–azure-sub-policy-compliance -dashboard.png)

### Tag Policy Compliance

Shows the **Require a tag on resources** policy at 100% compliance (7 of 7 resources).

![Tag Policy Compliance](screenshots/07-azure-sub-policy-require-tag-compliance.png)

### Resource Compliance

Shows the seven individual resources marked Compliant.

![Resource Compliance](screenshots/08-azure-sub-policy-require-tag-resource-compliance.png)

### PowerShell Verification

Shows PowerShell confirming seven compliant resources and zero non-compliant resources for the tag policy assignment.

![PowerShell Verification](screenshots/09-azure-sub-policy-powershell-compliance-verification.png)
