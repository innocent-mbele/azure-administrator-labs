@'
# Microsoft Entra ID — Users, Groups and Audit Logs

## Overview

This lab demonstrates the administration of users and security groups in the default Microsoft Entra ID tenant.

A sample employee account, Sibusiso Ndlovu, was created with organisational profile information and added to the IT-Cloud-Ops security group.

The lab also examines Microsoft Entra ID directory roles, sign-in logs and audit logs. Audit events were reviewed to identify the initiating administrator, affected target objects, modified properties and operation status.

Group membership was subsequently verified in the Azure portal.

## Screenshots

### Default Tenant Overview

Shows the Default Directory tenant overview, including its tenant information and Microsoft Entra ID Free licence.

![Default Tenant Overview](screenshots/01-entra-tenant-overview)

---

### Global Administrator Role

Shows the Global Administrator directory role assigned to the administrator account.

![Global Administrator Role](screenshots/02-entra-global-administrator-role)

---

### User Created

Shows the Sibusiso Ndlovu user account created in Microsoft Entra ID.

![User Created](screenshots/03-entra-user-created)

---

### Security Group Created

Shows the IT-Cloud-Ops security group and its configuration.

![Security Group Created](screenshots/04-entra-security-group-created)

---

### Audit Logs

Shows the tenant audit log records generated during the user and group administration activities.

![Audit Logs](screenshots/05-entra-audit-logs)

---

### User Creation — Audit Targets

Shows the target information recorded for the successful Add user audit event.

![User Creation Audit Targets](screenshots/06-entra-audit-user-creation-targets)

---

### User Creation — Modified Properties

Shows the properties recorded as changed during user creation, including account status and employee profile attributes.

![User Creation Modified Properties](screenshots/07-entra-audit-user-creation-modified-properties)

---

### Group Membership — Audit Targets

Shows the user and security group identified as targets in the successful Add member to group audit event.

![Group Membership Audit Targets](screenshots/08-entra-audit-group-membership-targets)

---

### Group Membership — Modified Properties

Shows the group properties recorded in the audit event, including the group Object ID and display name.

![Group Membership Modified Properties](screenshots/09-entra-audit-group-membership-modified-properties)

---

### Group Membership Verified

Shows Sibusiso Ndlovu listed as the member of the IT-Cloud-Ops security group, confirming the membership operation.

![Group Membership Verified](screenshots/10-entra-group-membership-verified)
'@ | Set-Content -Path "README.md" -Encoding utf8