---
layout: post
title: "My 5 Must-Have GAM Commands for Managing Google Workspace"
date: 2025-09-01
category: Technical
feature_image: feature-cli
author_name: Hichem
author_url: /about/
author_avatar: hichem
desc: "A practical guide to the top 5 GAM commands for Google Workspace administrators. Learn how to automate bulk user creation, group management, file transfers, and more to save time and manage your domain at scale."
---
*My go-to commands for Google Workspace automation.*

Here are five essential [GAM](https://github.com/GAM-team/GAM){:target="_blank" rel="noopener noreferrer"} commands that save time and streamline common administrative tasks in Google Workspace. Each one tackles a frequent challenge that can be slow and repetitive when done through the Admin Console UI.

---

### 1. Bulk User Creation from a CSV

This is the cornerstone of automating onboarding. Instead of creating users one-by-one in the Admin Console, you can create hundreds from a single CSV file, which you can prepare in a spreadsheet application.

**Why it's a must-have:** 
It turns the time-consuming task of new hire setup into a simple, repeatable process, ensuring consistency and saving massive amounts of time.

**Example command:**
    ```gam csv users.csv gam create user ~Email firstname ~FirstName lastname ~LastName password ~Password org ~OrgUnit changepassword on
    ```

The ```gam csv users.csv``` command will indicate GAM that it needs to look for the users.csv file for data.

The parameters ```~Email``` and other parameters with the ```~``` are variables, and basically indicate GAM that it need to replace the variable with the items from the csv file.

To sumarize, the command:\
```gam csv users.csv gam create user ~Email firstname ~FirstName lastname ~LastName password ~Password org ~OrgUnit changepassword on ```

will act as:\
```gam create user hichem@company.com firstname Hichem lastname BM password 1234 org /Employee changepassword on
``` and so on for evey line of the csv file.

---

### 2. Bulk Group Membership Management

Managing group memberships is a constant task, from adding new hires to project teams to updating distribution lists. This command allows you to add or remove users from groups in bulk using a simple list.

**Why it's a must-have:** 
It simplifies access control and communication management, eliminating the tedious process of searching for users and adding them to groups manually.

**Example command:**
    ```gam csv new_sales_hires.csv gam update group sales-team@yourdomain.com add member user ~Email
    ```

---

### 3. Transfer Google Drive Ownership on Offboarding

When a user leaves the company, ensuring their work files are retained is critical. This command transfers all of a user's Drive files to their manager or a successor, a key step in any offboarding workflow.

**Why it's a must-have:** 
It's a crucial data security and business continuity command. It prevents data loss and ensures a smooth handover of responsibilities when an employee departs.

**Example command:**
    ```gam user departing.user@yourdomain.com transfer drive to new.owner@yourdomain.com
    ```

---

### 4. Move a Single User Between Organizational Units (OUs)

When an employee changes roles or departments, they often need to be moved to a new Organizational Unit to inherit the correct settings and policies. This command makes that move instantaneous.

**Why it's a must-have:** 
It’s a fast and scriptable way to handle individual user moves without navigating through the Admin Console UI, making it perfect for quick helpdesk tickets or one-off organizational changes.

**Example command:**
    ```gam update user employee@yourdomain.com org "/Sales/WestCoast"
    ```

---

### 5. Manage a User's Inbox Delegation

Setting up inbox delegation is a common request for executive assistants or for covering an employee's leave. This command lets you grant access directly from the command line.

**Why it's a must-have:** 
It provides a precise, one-line solution for a frequent administrative task, saving you from having to go through multiple clicks in the Gmail settings of a user's account.

**Example command:**
    ```gam user manager@yourdomain.com add delegate assistant@yourdomain.com
    ```
