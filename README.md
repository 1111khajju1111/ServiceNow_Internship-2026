# ServiceNow_Internship-2026
Optimizing User, Group, and Role Management with Access Control and Workflows


# Optimizing User, Group, and Role Management with Access Control and Workflows

## Overview

This ServiceNow project focuses on implementing **role-based user, group, and access control management** to improve task assignment, accountability, and workflow efficiency within a small project team.

The system defines distinct roles for **Project Manager** and **Team Member**, ensuring that users have appropriate permissions based on their responsibilities. Access Controls (ACLs) and workflows are configured to prevent unauthorized actions while enabling smooth collaboration, task management, and project tracking.

---

## Workspace

**Workspace Type:** Kanban  
**Application Area:** Information Technology  

---

## Objectives

- Implement role-based access control in ServiceNow.
- Manage users, groups, and roles efficiently.
- Restrict unauthorized access to project and task records.
- Enable structured project and task assignment workflows.
- Improve accountability through controlled permissions.
- Automate project lifecycle activities using workflows.

---

## Roles and Responsibilities

### Project Manager Role

**Responsibilities:**
- Create and manage projects.
- Assign tasks to team members.
- Monitor project progress.
- Update project and task statuses.
- Review team member activities.

**Permissions:**
- Create Project records.
- Read and update project details.
- Assign tasks.
- View team performance and progress.

---

### Team Member Role

**Responsibilities:**
- View assigned tasks.
- Update task progress.
- Maintain task status.
- Provide completion updates.

**Permissions:**
- View assigned tasks.
- Update task status and progress.
- Add task-related information.

**Restrictions:**
- Cannot create projects.
- Cannot modify project ownership.
- Cannot access unauthorized records.

---

# Implementation Details

## 1. User Management

Users are created and assigned appropriate roles based on their responsibilities.

### Users Created:
- Project Manager
- Team Members

Each user is mapped to specific groups and roles to control access permissions.

---

## 2. Group Management

Groups are created to organize users and simplify permission management.

### Groups:

**Project Management Group**
- Contains Project Managers.
- Responsible for project creation and monitoring.

**Development Team Group**
- Contains Team Members.
- Responsible for completing assigned tasks.

---

## 3. Role Management

Custom roles are created for controlled access.

### Custom Roles:

| Role | Purpose |
|------|---------|
| Project Manager | Manage projects, assign tasks, monitor progress |
| Team Member | Work on assigned tasks and update status |

---

# Access Control (ACL) Implementation

Access Control Lists are configured to secure application data.

## Project Table ACL

### Create Access
- Allowed for: Project Manager Role
- Restricted for: Team Member Role

### Read Access
- Allowed for:
  - Project Manager
  - Assigned Team Members

### Update Access
- Allowed for:
  - Project Manager
  - Authorized users

### Delete Access
- Restricted to Project Manager only.

---

## Task Table ACL

### Create Task
- Allowed for Project Manager.

### Update Task
- Allowed for:
  - Assigned Team Members
  - Project Manager

### Read Task
- Users can view only authorized tasks.

---

# Workflow Automation

Workflows are created to automate project and task lifecycle management.

## Project Workflow

### Flow:

1. Project Manager creates a project.
2. Project details are reviewed.
3. Tasks are created and assigned.
4. Team members receive task notifications.
5. Members update task progress.
6. Project Manager monitors completion.

---

## Task Assignment Workflow

### Flow:

```

Task Created
|
↓
Assigned to Team Member
|
↓
Notification Sent
|
↓
Member Updates Status
|
↓
Project Manager Reviews Progress

```

---

# Features Implemented

✅ User creation and management  
✅ Group-based access control  
✅ Custom role creation  
✅ Role-based permissions  
✅ ACL security implementation  
✅ Project and task management  
✅ Automated workflow execution  
✅ Task assignment notifications  
✅ Progress tracking  

---

# Security Benefits

- Prevents unauthorized data modification.
- Ensures users access only required information.
- Improves data security through role-based permissions.
- Maintains accountability for project activities.

---

# Technologies Used

| Technology | Purpose |
|------------|---------|
| ServiceNow | IT Service Management Platform |
| Users | Identity Management |
| Groups | User Organization |
| Roles | Permission Management |
| ACL | Data Security |
| Flow Designer / Workflow | Process Automation |

---

# Project Outcome

The implementation provides a secure and efficient project management environment in ServiceNow by combining **User Management, Group Management, Role-Based Access Control, ACL Security, and Workflow Automation**.

The solution ensures that project activities are properly controlled, tasks are assigned efficiently, and team members can collaborate while maintaining data security and accountability.
