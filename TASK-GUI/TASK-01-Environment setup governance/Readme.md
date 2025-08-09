# Task 01 – Environment Setup & Governance

This guide outlines how to set up Microsoft Teams for organizational use and apply governance controls using the Microsoft 365 Admin Center and Microsoft Entra admin center. All steps are portal-based and require no scripting.

## Objective

- Create Teams for organizational units (e.g., Team1, Team2)
- Apply consistent naming conventions using Microsoft Entra ID group policies
- Configure expiration policies to manage inactive Teams

## Prerequisites

- Admin access to Microsoft 365 Admin Center
- Microsoft Entra ID P1 license (for expiration policies and naming conventions)
- Access to Microsoft Entra admin center

## Steps

### 1. Create Teams

Navigation:  
Microsoft Teams Admin Center → Teams → Manage Teams → + Add

Steps:
1. Click + Add to create a new Team.
2. Choose "Create a team from scratch" or "Create from an existing group".
3. Enter a name for the Team (e.g., Team1, Team2).
4. Assign Owner
5. Set privacy level (Public or Private).
   
   * Private teams aren't open for everyone to join them and team owners are the only ones that can add members to them.
         These teams won't show up in search results or in the Teams gallery.
   
   * Public teams can be seen by everyone from the Teams gallery and people can join them without getting approval from a team owner.
       
     
---

Screenshot:
<img width="1908" height="853" alt="image" src="https://github.com/user-attachments/assets/abcc6e4d-5712-487a-8234-bfbea5cb7775" />

---

## Task 02: Configure Group Naming Policy

This task sets up a naming policy for Microsoft 365 Groups (including Teams) to enforce consistent naming formats and block reserved or inappropriate terms.

### Navigation

1. Go to **Groups → Naming Policy**.

2. In the **PrefixSuffixNamingRequirement** field, define a format using:
   - Static text (e.g., `Team-`)
   - Supported attributes (e.g., `[Department]`)

   **Example format:**
   
    <img width="1102" height="807" alt="image" src="https://github.com/user-attachments/assets/8531ed43-72e4-45ee-9552-e71c57a113d0" />

    Output result:
   
    <img width="443" height="601" alt="image" src="https://github.com/user-attachments/assets/96de1ce2-b239-42d6-ace7-3aaa306fbcb6" />


Note: Naming policies only apply to new groups created after the policy is set.

3. Under **Blocked Words**, upload a CSV file to prevent use of reserved or sensitive terms.

- The file must be plain text, with **one word per line**.
- No headers, quotes, or commas.
  
  <img width="852" height="237" alt="image" src="https://github.com/user-attachments/assets/9bdf2823-eed7-49b2-ae89-9a9cbad4ab94" />
  
4. Save the policy. It will apply to all newly created Microsoft 365 Groups (including Teams).

> ⚠️ Naming policies apply only to Microsoft 365 Groups created by end users through apps like Teams, Outlook, or Planner.  
> Groups created by administrators via Entra admin center, PowerShell, or Graph API are **not subject to naming policy enforcement**.

 Output result:

 <img width="745" height="735" alt="image" src="https://github.com/user-attachments/assets/d8061580-82a2-4a29-8d2b-b137ee2d9c19" />

  ---
  
### 3. Configure Teams Expiration Policies

Navigation:  
Microsoft Entra admin center → Groups → Expiration

Steps:
1. Go to Groups → Expiration.
2. Enable expiration for Microsoft 365 Groups.
3. Set the default expiration period (e.g., 180 days).
4. Configure notification settings for group owners.

Screenshot: 

Best Practice:  
Use expiration policies to clean up unused Teams and reduce clutter. Group owners will be notified before deletion and can renew the group.

## Outcome

- Teams created with consistent naming conventions
- Governance policies applied to prevent sprawl
- Expiration policies in place to manage lifecycle

---
