# Azure-Operations-Governance-Fundamentals
Hands-on exploration of Azure operational governance, compliance, cost management, availability planning, and support processes as part of the AZ‑900 learning path.

## Overview
This repository documents hands-on labs focused on Azure operational governance and management completed as part of the AZ-900T00-A Introduction to Microsoft Azure course.

The labs explore how organizations manage compliance, cost, availability, and support in Azure environments. The labs also demonstrate how to apply governance, organization, and protection mechanisms across Azure resources using **tags** and **resource locks**.

---

## Labs Covered

### Compliance & Trust
- Explored Microsoft Compliance Offerings
- Accessed the Service Trust Portal (STP)
- Reviewed compliance documentation and audit reports
- Used Compliance Manager to assess cloud compliance posture

### Cost Management & Planning
- Estimated Azure infrastructure costs using the Pricing Calculator
- Compared on-premises and Azure costs using the TCO Calculator
- Generated and reviewed cost estimation and savings reports

### Availability & Reliability
- Reviewed SLA uptime guarantees for Azure services
- Calculated composite SLA for a multi-service application
- Understood how service dependencies affect overall availability

### Azure Support & Operations
- Reviewed Azure support plan options
- Practiced creating and monitoring billing and support requests
- Gained operational awareness of Azure support processes

#### Alerts & Operational Notifications

##### Objectives
- Configure action groups for alert notifications  
- Create Service Health alerts for platform incidents  
- Create Activity Log alerts for operational visibility  

##### Tasks Performed

###### 1. Create an Action Group
- Configured an action group with email notifications and validated delivery through a test alert.

**Outcome:**  
An action group configured to send email notifications when alerts fire.

###### 2. Create a Service Health Alert
- Created a Service Health alert to monitor Azure platform incidents and planned maintenance in selected regions.

**Outcome:**  
A Service Health alert that notifies the operations team about Azure platform issues and maintenance events.

###### 3. Create an Activity Log Alert
- Configured an Activity Log alert that triggers when any resource is deleted in the monitored resource group.

**Outcome:**  
An Activity Log alert that provides real‑time visibility into resource deletions within the environment.  

### Create Resources and Apply Tags

#### Objectives
- Create a resource group and multiple storage accounts  
- Apply consistent organizational tags  
- Use tag-based filtering to locate and organize resources  

#### Tasks Performed

##### 1. Prepare the Environment
- Created a dedicated resource group for governance testing.
- Ensured subscription and region alignment.

##### 2. Create a Test Storage Account
- Deployed the first storage account inside the resource group.

##### 3. Tag the Resource Group
Applied tags such as:
- `Environment: Test`
- `Department: IT`
- `Owner: Admin`

##### 4. Tag the Storage Account
- Added matching tags to ensure consistency and support cost allocation.

##### 5. Create a Second Storage Account with Different Tags
- Deployed a second storage account with alternate tags (e.g., `Environment: Dev`).

##### 6. Filter Resources by Tag
- Used Azure Portal filtering to quickly locate resources based on tag values.
- Demonstrated how tags improve visibility in large environments.

**Outcome:**  
A resource group and two storage accounts with consistent and meaningful organizational tags applied.

---

### Apply Resource Locks

#### Objectives
- Protect critical resources from accidental modification or deletion  
- Understand the difference between **Delete** and **Read‑only** locks  

#### Tasks Performed

##### 1. Apply a Delete Lock to the Storage Account
- Added a **Delete** lock to prevent accidental removal of the storage account.

##### 2. Apply a Read‑Only Lock to the Resource Group
- Applied a **Read‑only** lock at the resource group level.
- Ensured all resources inside the group inherit the lock restrictions.

**Outcome:**  
A storage account protected by a delete lock and a resource group protected by a read‑only lock.

---

### Test Lock Enforcement

#### Objectives
- Validate how Azure enforces locks  
- Confirm that locks override user permissions  
- Restore normal operations by removing locks  

#### Tasks Performed

##### 1. Test the Read‑Only Lock
- Attempted to modify resources inside the locked resource group.
- Azure correctly blocked all write operations.

##### 2. Test the Delete Lock
- Attempted to delete the locked storage account.
- Azure prevented the deletion and displayed lock enforcement messages.

##### 3. Remove the Locks
- Removed both locks to restore normal functionality.

##### 4. Confirm Normal Operations Are Restored
- Successfully modified and deleted resources after lock removal.

**Outcome:**  
Confirmed that Azure locks prevent changes as expected and that removing locks restores full administrative access.

---

### Cost Governance: Tags, Budgets & Azure Policy

#### Objectives
- Apply cost‑tracking tags to pilot resources  
- Configure budgets and alert thresholds  
- Assign and validate Azure Policy for governance enforcement  

#### Tasks Performed

##### 1. Apply Cost‑Tracking Tags
- Created a resource group and storage account for cost governance testing.
- Applied organizational tags to both resources to support cost reporting and filtering.

**Outcome:**  
Tagged pilot resources ready for cost reporting and filtering.

##### 2. Create Budget and Alerts
- Configured a budget with alert thresholds to provide early warnings before spending exceeds targets.
- Enabled actionable notifications to support proactive cost management.

**Outcome:**  
Budget thresholds configured with automated alerts for cost monitoring.

##### 3. Assign and Test Azure Policy
- Assigned a policy restricting resource creation to a specific region.
- Validated that non‑compliant deployments were blocked.
- Reviewed the compliance dashboard to confirm enforcement.

**Outcome:**  
A policy control assigned and validated through a compliance test, demonstrating preventative governance.

---

## Key Learnings
- Azure provides built-in tools for compliance, trust, and risk management.
- Cost estimation and comparison are essential before cloud deployment.
- Application availability depends on the combined SLAs of all services.
- Azure offers structured support models for technical and billing issues.
- Operational governance is a core part of cloud management.

---

## Skills Demonstrated
- Azure Governance & Compliance
- Cost Estimation & TCO Analysis
- SLA & Availability Planning
- Azure Support & Operations
- Cloud Financial Management
- Resource Tagging Strategy  
- Resource Locks (Delete / Read‑only)  
- Operational Safety & Change Control 

---

## Next Steps
- Prepare for the AZ-900 certification exam
- Apply governance and cost management concepts in real-world scenarios
- Continue learning toward Azure Administrator (AZ-104)

