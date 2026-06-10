# ServiceNow ITSM Lab

This repository documents a hands‑on ServiceNow IT Service Management (ITSM) lab demonstrating practical experience with **Incidents, Problems, Changes, Service Catalog, Approvals, Reporting, and ITIL processes** using a free Personal Developer Instance (PDI).

---

## 📌 Lab Overview

This lab covers:

- Setting up a free ServiceNow developer instance  
- Navigating core ITSM modules  
- Creating and resolving an Incident  
- Building a Service Catalog item  
- Creating a Change Request with approval workflow  
- Generating ITSM reports  
- Mapping activities to ITIL concepts  

This project serves as a portfolio‑ready demonstration of real ServiceNow administration skills.

---

## 🧩 1. Get Your Free ServiceNow Instance

1. Go to **https://developer.servicenow.com**
2. Create a free account
3. Select **Request Instance**
4. Choose the latest stable release (Washington or newer)
5. Wait 10–15 minutes for provisioning
6. You will receive:
   - Instance URL (e.g., `https://dev12345.service-now.com`)
   - Admin credentials

> **Note:** PDIs hibernate after 10 days and are reclaimed after 30 days. Log in weekly to keep your work.

---

## 🧭 2. Platform Navigation

Key modules used in this lab:

| Module | Location | Purpose |
|--------|----------|---------|
| **Incident** | Service Desk → Incidents | Break/fix ticketing |
| **Problem** | Service Desk → Problems | Root cause analysis |
| **Change** | Change → Changes | Planned modifications |
| **Service Catalog** | Service Catalog → Catalogs | User request portal |
| **Reports** | Reports → Create New | Dashboards & analytics |
| **Flow Designer** | Process Automation → Flow Designer | Workflow automation |

---

## 🛠️ 3. Create & Work an Incident

### Create the Incident

Path: **Service Desk → Incidents → New**

| Field | Value |
|-------|--------|
| Caller | Abel Tuter |
| Category | Software |
| Subcategory | Email |
| Short description | User cannot access Outlook — cannot connect to server |
| Description | Outlook stopped working at ~9 AM. Error: “Cannot connect to the Exchange server.” User on Wi‑Fi. No other users affected. |
| Priority | 3 — Moderate |
| Assignment Group | Service Desk |

Submit and note the generated ticket number (e.g., `INC0001234`).

---

### Work the Incident

1. Open the incident  
2. Set **State → In Progress**  
3. Assign to yourself  
4. Add **Work Notes**:

Contacted user. Confirmed error message. Outlook profile appears corrupted.
Attempting profile repair. User instructed to use OWA temporarily.
ETA: 30 minute


5. Add **Resolution Notes**:

Rebuilt Outlook profile. Removed and re-added the Exchange account.
User confirmed Outlook is working. Issue caused by corrupted OST file.


6. Set **State → Resolved**, then **Closed**

---

## 💻 4. Build a Service Catalog Item

### Create a Laptop Request Item

Path: **Service Catalog → Catalogs → Service Catalog → Maintain Items → New**

| Field | Value |
|--------|--------|
| Name | New Laptop Request |
| Category | Hardware |
| Short description | Request a new or replacement laptop |
| Description | Form for new‑hire laptops or replacements. Reviewed within 2 business days. Delivery: 5–7 days after approval. |
| Fulfillment group | IT Hardware Team |
| Price | (leave blank) |

### Add Variables

| Variable | Type | Mandatory |
|----------|-------|-----------|
| Requester Name | Single Line Text | Yes |
| Business Justification | Multi Line Text | Yes |
| Required By Date | Date | Yes |
| Laptop Model Preference | Select Box (Standard, Developer, Executive) | No |

Preview to confirm it appears in the Service Catalog.

---

## 🔐 5. Create a Change Approval Workflow

### Create a Standard Change Request

Path: **Change → Changes → New (Standard)**

| Field | Value |
|--------|--------|
| Short description | Deploy security patch MS24‑001 to all Windows workstations |
| Category | Software |
| Risk | Low |
| Impact | 2 — Medium |
| Start date | Next Saturday, 2:00 AM |
| End date | Next Saturday, 6:00 AM |
| Description | Monthly patch deployment via WSUS. Addresses CVE‑2024‑0001 (CVSS 7.8). One reboot required. Rollback: uninstall via WSUS if issues occur. |

Add **Test Plan** and **Backout Plan** under the Planning tab.

Click **Request Approval**, then approve it as admin.  
The Change moves to **Scheduled**.

---

## 📊 6. Build ITSM Reports

### Report: Incident Volume by Priority (Last 30 Days)

- Name: **Incident Volume by Priority — Last 30 Days**
- Table: **Incident**
- Type: **Bar Chart**
- Group by: **Priority**
- Condition: **Created ≥ 30 days ago**

### Additional Reports

- **Mean Time to Resolution (MTTR)** — grouped by Assignment Group  
- **Open Incidents by Assigned Agent** — workload visibility  

---

## 📘 7. ITIL Concepts Demonstrated

| ITIL Term | Definition | ServiceNow Module |
|-----------|------------|-------------------|
| **Incident** | Unplanned interruption; restore service quickly | Incidents |
| **Problem** | Root cause of recurring incidents | Problems |
| **Change** | Planned modification with risk control | Changes |
| **Service Request** | Request for something new | Service Catalog |
| **SLA** | Response/resolution time commitments | SLA Definitions |
| **CMDB** | Asset & relationship database | Configuration Items |
| **Knowledge** | Articles for known issues | Knowledge Base |

---

## 📁 Portfolio Deliverables

Include screenshots of:

- ✔️ Completed Incident (with work notes + resolution)  
- ✔️ Service Catalog Item  
- ✔️ Change Request with approval workflow  
- ✔️ One dashboard/report  

For each screenshot, include a short paragraph explaining:

- What ITIL process it represents  
- Why it matters in IT operations  
- How ServiceNow supports that workflow  

---

