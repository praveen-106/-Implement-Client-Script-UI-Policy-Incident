# ServiceNow: Implement Client Script & UI Policy (Incident)

This repository contains configuration XMLs, Client Scripts, screenshots, and technical documentation for implementing client-side validation and automated UI policies on the **Incident (`incident`)** table in ServiceNow.

---

## 🎥 Demo Video

[▶️ Watch the ServiceNow Project Demo](https://drive.google.com/file/d/15gM7HQOo1h89jvKIvfGeAJilgFdY3sG_/view)

---

## 📌 Project Overview

The objective of this project is to enforce dynamic business logic, automated field dependencies, form submission validations, and list-view editing restrictions on ServiceNow Incident records.

### Key Deliverables & Features
* **UI Policy (`High Impact Control`)**: Automatically triggers when an Incident's `Impact` is set to `1 - High`.
* **UI Policy Action**: Enforces the `Urgency` field to be **Read-only** when High Impact conditions are met.
* **`onChange` Client Script**: Automatically sets `Urgency` to `1 - High` and displays an informational message when `Impact` changes to High.
* **`onSubmit` Client Script**: Validates that `Assigned To` is populated before submitting high-impact incidents, displaying an inline error box if missing.
* **`onCellEdit` Client Script**: Blocks unauthorized inline updates to the `State` field directly from the Incident list view.

---

## 👥 Team Members & Roles

* **Nishanth T** — UI Policy Configuration & List Edit Client Script Development
* **Ranjith S** — UI Policy Actions Configuration & Testing Suite Execution
* **Ravichandran K** — `onChange` Client Script Implementation & Validation
* **Ronald Paul Sebastin A** — `onSubmit` Save Validation Scripting & Reverse Testing

---

## 📁 Repository Directory Structure

```text
Implement-Client-Script-UI-Policy-Incident/
│
├── README.md
├── docs/
│   ├── ServiceNow_Project_Documentation.docx
│   └── ServiceNow_Project_Documentation.pdf
│
├── client_scripts/
│   ├── onChange_AutoSetUrgencyForHighImpact.js
│   ├── onSubmit_PreventSaveIfAssignedToMissing.js
│   └── onCellEdit_PreventStateChangeViaListEdit.js
│
├── ui_policies/
│   ├── sys_ui_policy_High_Impact_Control.xml
│   └── sys_ui_policy_action_Urgency_ReadOnly.xml
│
└── Screenshots
