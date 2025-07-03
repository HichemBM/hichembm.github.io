---
layout: post
title: "Case Study: Orchestrating the Drivy-Getaround Google Workspace Merger"
date: 2019-09-05
categories: Drivy Getaround
author_name: Hichem
author_url: /about/
author_avatar: hichem
feature_image: getaround-merger-2
---

In the summer of 2019, following the acquisition of Drivy by its US competitor Getaround, I was faced with the most defining project of my career. 

As the sole IT Manager for Drivy in Europe, and with Getaround having no dedicated IT staff at the time, the responsibility for the initial, critical phase of the merger (the integration of our core IT systems- fell on my shoulders. The very first, and most foundational, piece of this puzzle was merging our two distinct Google Workspace environments.

### The Strategic Challenge: More Than Just a Data Migration

The objective was technically complex but strategically vital: migrate all 200+ Drivy user accounts—including every email, calendar event, and Drive file—into the larger, 1100-user Getaround instance. 

This wasn't just a data transfer; it was about laying the technical groundwork for unifying two distinct company cultures across continents. The project timeline was aggressive, driven by pressing marketing and business objectives that required a swift and seamless integration.

Given the scale and tight deadlines, I made the strategic decision to partner with a third-party specialist, [Devoteam G Cloud](https://gcloud.devoteam.com/), to assist with the raw data migration. 

However, my role was to be the project's chief architect and conductor, orchestrating every facet of the merger from planning and vendor management to technical execution and change management.

### The Project Lifecycle: A Blend of Technical Mastery and Strategic Oversight

I designed and managed a multi-phased project plan that prioritized risk mitigation and minimal user disruption.

**1. Discovery, Planning, and Vendor Management:**

The project began with a meticulous audit of both Google Workspace environments. 
On the Drivy side, we had a primary domain with five aliases and critical integrations with CRMs like Zendesk. The Getaround side was a much larger, global instance. 

I established a clear project governance structure, set up technical workshops, and defined the migration strategy. This foundational work formed the basis of the RFP for our third-party partner and ensured a smooth collaboration with Devoteam.

**2. Technical Execution & The Role of GAM:**
While our partner handled the "migration factory" setup, my hands-on technical expertise was crucial for managing the user-side operations. 

I extensively used **[GAM](https://github.com/GAM-team/GAM)**, a command-line tool, to perform critical batch operations that were outside the scope of the migration tools.

This included creating and mapping user accounts, managing groups with specific parameters, and executing the complex user renaming process during the final cutover. 

My proficiency with GAM was instrumental in managing the ~200 Drivy accounts and integrating them into the larger ~1100 user Getaround environment efficiently and without error.

**3. Phased Migration & Change Management:**
To minimize risk, we executed the migration in carefully planned stages:

* **Pre-Migration:** We first migrated all "cold" data older than 60 days to move the bulk of information without impacting active work.
* **Delta Migration:** Subsequent passes migrated more recent data, which I scheduled after work hours to avoid disruption.
* **The Cutover:** The final migration and switchover were meticulously planned for the last weekend of August, a period of lower activity that would minimize business impact.

Communication was paramount. I developed a multi-channel communication plan using a mix of **asynchronous** (Slack, email, a dedicated Google Sites wiki for all information) and **synchronous** (weekly stand-ups, company-wide All-Hands meetings) methods to keep every stakeholder informed and to prepare users for the change.

### The Outcome: A 99.9% Success Rate and a Unified Company

The project was completed on schedule and achieved a **99.90% success rate** in data migration. The only notable issue involved a handful of legacy Google Sites V1 pages that were incompatible with the migration tools. Even then, I was able to manually rebuild and recover approximately 60% of this content from archives and backups, ensuring minimal data loss.

Beyond the technical success, the true result was cultural. The unified Google Workspace instance became a key milestone in the merger. It broke down geographical barriers, enabled seamless cross-continental collaboration from day one, and was a powerful symbol of our new, integrated company identity. 

This project was a testament to the power of combining deep technical knowledge with strategic project management to navigate one of the most critical phases of a corporate acquisition.