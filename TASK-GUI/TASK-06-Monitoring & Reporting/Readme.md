# Task 06 – Monitoring & Reporting

## Objective
Track Microsoft Teams usage and export activity logs to support governance, auditing, and lifecycle decisions. This task is fully validated using the Teams Admin Center and Microsoft 365 Compliance portal.

---

## Validation Steps

### 1. Generate Teams Usage Reports

- Navigate to **Teams Admin Center** → **Analytics & reports** → **Usage reports**
- Select **Teams usage** or **User activity**
- Choose a relevant **date range** and click **Run report**
  
  <img width="1862" height="857" alt="image" src="https://github.com/user-attachments/assets/014a6e2e-97b7-42d8-a2b1-e50e0e606a0f" />

  <img width="1918" height="803" alt="image" src="https://github.com/user-attachments/assets/03b2ef54-ec37-42d3-b1f1-49f8e714fa3f" />


### 2. Export Teams Activity Logs

- Navigate to **Microsoft Purview portal** → **Solutions** → **Audit**
- Use filters to search for:
  - `Created team`
  - `Added member to team`
  - `Deleted channel`
  - Export results as `.csv`. (export is available if role assigned)

  <img width="1837" height="852" alt="image" src="https://github.com/user-attachments/assets/d641353c-dfdf-4c52-b7e2-561030489251" />


---

## Notes

- Audit logging is enabled by default in Microsoft 365 tenants. No manual setup is required.

- Export functionality requires assignment to the Audit Reader or Audit Manager role group in Purview.

- Reports may take time to populate based on tenant activity and licensing tier.

- Audit logs are essential for tracking lifecycle events, membership changes, and policy enforcement.

---

## Outcome Summary

Step Validated 

 - Teams usage report generated
 - Audit log searched with filters
 - Audit log export available (requires role assignment)

---

## Scope
This task is native to the **Teams Admin Center** and **Microsoft Purview portal**. 

---

### Important Note:

Role-Based Access in Microsoft Purview
Microsoft Purview enforces role-based access control for all portal actions. Even Global Administrators must be explicitly assigned to relevant Purview role groups to access features such as audit search, data classification, policy management, and export functions.

Role assignment is managed under Settings → Roles and scopes in the Purview portal. Access changes may require sign-out/sign-in to take effect.
