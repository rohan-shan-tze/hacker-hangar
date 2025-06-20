---
layout: single
title: Change Management
date: 2025-06-20
author_profile: true
read_time: true
tags:
  - Security+
  - fundamentals
  - change
  - management
excerpt: An outline of how changes are managed professionally in an organisation.
---
Changes are important. They introduce new features and fix old bugs and vulnerabilities. But in a system with a myriad of devices, how can we implement these changes in a safe and reliable way?

---

### Management Perspective

Here we discuss the change management process from the perspective of the managers and business people.

- Approval Process: A change designed by a technician should be analysed and approved by at least one other person.   
- Ownership: The entity that "owns" the change process. For example, a department that requested a change in an application would be the owner. Typically not the entity that implements the change.
- Stakeholders: Anybody affected by the change
- Impact Analysis: Analyse the scope and risk of the proposed change. 
- Test Results: Test the change in a safe environment (like a sandbox) before rolling out.
- Backout Plan: Have a plan to revert the system to its original or similar state in case the change causes problems.
- Maintenance Window: The scheduled time during which the update is implemented
- Standard Operating Procedure: Change process should be adequately documented.

### Technician Perspective

- Allow List: A list of applications that are allowed, all other applications are blocked. A technician may be required to change an Allow List or follow an Allow List while changing the system
- Deny List: The opposite of an Allow List, permits all applications except explicitly denied. Allows more flexibility than an Allow List. 
- Restricted activities: The scope that the technician is allowed to make changes to is important. Areas outside the scope should be untouched.
- Downtime: May be required for update to be implemented. Typically choose off-working hours to not disrupt workers. And off-peak season to prevent risk of affecting customers at critical times. If it is a 24-hour business, the team may choose to make a copy of the system to perform updates without disrupting live operations. This 2 system method also provides a simple Backout Plan. It is good practice to inform organisation and customers of downtime, this can be done via email.
- Service/Application Restart: Some updates require restarting the service or application
- Legacy Applications: Technicians should document Legacy Applications thoroughly to ensure they can be understood and maintained despite the lack of official support from the original developers.
- Dependencies: Some changes require changes in another part of the system, or require an installation of some other resource. This affects a change's scope
- Documentation: Ensure all changes are documented.
- Version Control: Useful to have a system where you can view the details of changes in the past and possess the capability to rollback to previous versions.
 