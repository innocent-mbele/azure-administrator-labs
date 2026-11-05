# Advanced Microsoft Entra ID Administration

## Overview

I explored advanced Microsoft Entra ID admin within an Azure tenant. This involved inspecting device join, registration and security settings, performing bulk user creation and managing security group membership. I created seven internal user accounts using the Microsoft Entra ID bulk user creation feature. Encountered a minor challenge when working with the CSV bulk operation as the portal did not provide clear confirmation of the operation results.

To fix this I then used Microsoft Graph PowerShell by following the guidance in Microsoft's documentation on Bulk operations service limitations from https://learn.microsoft.com/en-us/entra/fundamentals/bulk-operations-service-limitations?WT.mc_id=Portal-Microsoft_AAD_IAM. I then established a delegated Graph connection, retrieved and verified all the 7 user accounts and exported their profile information to CSV. I also created a separate security group and named it IT-Cloud-Ops-Automation using Microsoft Graph PowerShell and automated the addition of all 7 users. I independently retrieved the group membership to verify that all 7 accounts had been added successfully.

---

## Screenshots

### Device Join and Registration Settings

Shows the Microsoft Entra ID device join and registration configuration, including user permissions, MFA requirements and device limits.

![Device Join and Registration Settings](screenshots/01-entra-device-join-registration-settings.png)

---

### Local Administrator Settings

Shows the device local administrator settings configured within Microsoft Entra ID.

![Local Administrator Settings](screenshots/02-entra-local-admin-settings.png)

---

### Device Security Settings

Shows the Microsoft Entra LAPS and BitLocker recovery key security settings.

![Device Security Settings](screenshots/03-entra-device-security-settings.png)

---

### Bulk User Creation

Shows the seven internal user accounts created through the Microsoft Entra ID bulk user creation process.

![Bulk Users Created](screenshots/04-entra-bulk-users-created.png)

---

### Bulk Operation Preview

Shows the uploaded CSV file recorded in the Microsoft Entra ID bulk operation preview.

![Bulk Operation Preview](screenshots/05-entra-bulk-operation-preview.png)

---

### Microsoft Graph User Verification

Shows the seven bulk-created user accounts retrieved and verified using Microsoft Graph PowerShell, including their UPNs, departments and job titles.

![Graph Bulk Users Verification](screenshots/06-graph-bulk-users-verification.png)

---

### CSV Export Verification

Shows the exported user information imported back into PowerShell, confirming the seven user records and their profile attributes.

![Graph CSV Export Verification](screenshots/07-graph-csv-export-verification.png)

---

### Automated Group Membership Verification

Shows the seven users successfully added to the IT-Cloud-Ops-Automation security group using Microsoft Graph PowerShell and independently retrieved to verify group membership.

![Graph Group Membership Verification](screenshots/08-graph-group-membership-verification.png)
