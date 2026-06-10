# ServiceNow ITSM Lab — Architecture Diagram

This document provides a high‑level architecture view of the ServiceNow ITSM environment used in this lab.  
It illustrates how core ITIL processes interact within the ServiceNow platform and how data flows between modules.

---

## 🏗️ High‑Level Architecture 

<img width="1536" height="1024" alt="Copilot_20260610_105624" src="https://github.com/user-attachments/assets/c18873b6-b441-4978-b332-1fa8d4bc5359" />

---

## 🔍 Component Breakdown

### **1. ServiceNow Platform (PDI)**
The hosted environment where all ITSM modules, workflows, and data reside.  
This includes the UI, database, automation engine, and reporting tools.

---

### **2. Incident Management**
- Handles break/fix issues  
- Tracks assignment, SLA, work notes, and resolution  
- Feeds data into reporting and Problem Management  

**Data Flow:**  
User → Service Desk → Incident → Assignment → Resolution → Reporting

---

### **3. Problem Management**
- Identifies root causes of recurring incidents  
- Links multiple incidents to a single problem record  
- Supports long‑term stability and prevention  

**Data Flow:**  
Incident Trends → Problem → Root Cause → Knowledge Base

---

### **4. Change Management**
- Controls planned modifications to infrastructure  
- Requires approvals and risk assessment  
- Ensures changes are scheduled, tested, and documented  

**Data Flow:**  
Change Request → Approval Workflow → Implementation → Closure

---

### **5. Service Catalog**
- User‑facing portal for structured requests  
- Uses variables, forms, and fulfillment groups  
- Reduces manual ticket creation  

**Data Flow:**  
User Request → Catalog Item → Workflow → Fulfillment Group

---

### **6. Approvals Engine**
- Handles manager or CAB approvals  
- Integrated with Change, Catalog, and custom workflows  
- Ensures governance and compliance  

---

### **7. Flow Designer / Workflow Engine**
- Automates routing, notifications, and logic  
- Connects modules together  
- Powers approvals, fulfillment, and escalations  

---

### **8. Reporting & Dashboards**
- Visualizes operational metrics  
- Examples used in this lab:
  - Incident Volume by Priority  
  - MTTR by Assignment Group  
  - Open Incidents by Agent  

**Data Flow:**  
All Modules → Reporting → Dashboards → Insights

---

## 📘 Summary

This architecture demonstrates how ServiceNow integrates ITIL processes into a unified platform.  
Each module (Incident, Problem, Change, Catalog) interacts through workflows, approvals, and reporting to support efficient IT operations.

