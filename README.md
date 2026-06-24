# 🚀 Onboard360
### Complete Employee Lifecycle Automation

> *From offer letter to fully equipped workstation — automated, tracked, and stress-free.*

---

## What is Onboard360?

Onboard360 is a ServiceNow-based onboarding automation portal built to take the chaos out of welcoming new employees.

Think about what happens today when someone joins your organization. HR scrambles to create a record. The manager gets a message on Slack (or worse, an email buried in their inbox). IT waits for someone to tell them what laptop to assign. The new hire shows up on Day 1 and their email isn't ready yet.

Onboard360 fixes all of that. It connects HR, Management, and IT into a single, automated workflow — so by the time a new employee walks through the door, everything is ready and waiting for them.

<!-- 📸 SCREENSHOT: Homepage / Portal landing page overview -->
![Portal Overview](screenshots/portal-overview.png)

---

## The Problem It Solves

When onboarding is manual, things fall through the cracks. Here's what typically goes wrong:

- **HR** creates records by hand, one field at a time
- **Managers** approve requests over email with no tracking
- **IT** waits for a nudge before setting up email accounts or assigning devices
- **Nobody** has a clear view of where things stand
- **The new hire** wonders if anyone even knows they're starting

The result? Delayed onboarding, frustrated employees, and a first impression that's hard to recover from.

---

## How Onboard360 Works

The moment an onboarding request is submitted, a chain of automated steps kicks in:

```
New Employee Request Submitted
        ↓
  Record Created in System
        ↓
  Manager Reviews & Approves
        ↓
   HR Reviews & Approves
        ↓
  IT Tasks Auto-Generated
        ↓
   Laptop / Device Assigned
        ↓
   Company Email Created
        ↓
  Software Licenses Provisioned
        ↓
   Welcome Email Sent to Employee
        ↓
  Dashboard Updated in Real Time
```

Every step is logged, tracked, and visible. No chasing people down. No missed steps.

<!-- 📸 SCREENSHOT: Flow Designer — showing the full automated workflow -->
![Flow Designer Workflow](screenshots/flow-designer-workflow.png)

---

## Key Features

| Feature | What It Does |
|---|---|
| **Record Producer** | Lets anyone submit an onboarding request without needing direct table access |
| **Multi-Level Approvals** | Routes requests through Manager → HR in sequence, automatically |
| **Flow Designer Automation** | Triggers IT tasks, asset allocation, and notifications without manual intervention |
| **Asset Provisioning** | Tracks laptops, desktops, phones, and accessories assigned to each employee |
| **Software Allocation** | Assigns and logs licenses for tools like Office 365, Slack, GitHub, and more |
| **Role-Based Access Control** | Each role sees only what they need — nothing more, nothing less |
| **Automated Notifications** | Keeps everyone in the loop at every stage |
| **Daily Reminders** | A scheduled job nudges teams about pending requests every morning |
| **Live Dashboard** | One screen showing pending approvals, completed onboardings, and asset status |
| **Reports** | Department-wise breakdowns, asset allocation summaries, and status overviews |

---

## Database Structure

Onboard360 uses four purpose-built tables to keep everything organized:

### Employee Master (`x_company_employee_master`)
The heart of the system. Stores everything about the new hire — from personal details and department to their current onboarding status.

**Status lifecycle:** `Draft → Pending Manager Approval → Pending HR Approval → Approved → In Progress → Completed`

<!-- 📸 SCREENSHOT: Employee Master record form in ServiceNow -->
![Employee Master Form](screenshots/employee-master-form.png)

### Asset Allocation (`x_company_asset_allocation`)
Tracks every piece of hardware assigned to an employee: who got what, when, and who assigned it.

**Supported assets:** Laptop, Desktop, Mobile Phone, Monitor, Accessories

<!-- 📸 SCREENSHOT: Asset Allocation table / record view -->
![Asset Allocation](screenshots/asset-allocation.png)

### Software Allocation (`x_company_software_allocation`)
Logs software licenses provisioned per employee, including license keys and assignment dates.

**Supported tools:** Office 365, VS Code, ServiceNow, Slack, Jira, GitHub, Teams

<!-- 📸 SCREENSHOT: Software Allocation record view -->
![Software Allocation](screenshots/software-allocation.png)

### Onboarding Tasks (`x_company_onboarding_task`)
Keeps IT accountable with clearly assigned tasks, due dates, and status tracking for every onboarding.

<!-- 📸 SCREENSHOT: Onboarding Tasks list view with status and assignments -->
![Onboarding Tasks](screenshots/onboarding-tasks.png)

---

## Who Uses It

Onboard360 is designed around four roles, each with a tailored experience:

**HR Admin** — Creates and manages employee records, handles HR-level approvals, oversees the entire onboarding process.

**Manager** — Reviews and approves onboarding requests for their direct team members.

**IT Admin** — Picks up auto-generated IT tasks, assigns hardware, provisions software.

**Employee** — Logs in to see their own onboarding status, assigned assets, and progress — no back-and-forth needed.

---

## Security & Access Control

Access is tightly controlled through ServiceNow ACLs and custom roles. An employee can only see their own records. A manager sees their team. IT handles the technical provisioning side. HR has full visibility across the board.

Nothing leaks between roles. No one sees what they shouldn't.

<!-- 📸 SCREENSHOT: ACL / Role configuration in Studio or System Security -->
![Role-Based Access Control](screenshots/role-access-control.png)

---

## Notifications That Actually Help

Onboard360 sends targeted notifications at the right moments — not a flood of emails:

- **Approval Request** → Sent to the Manager when a new request arrives
- **HR Notification** → Triggered after Manager approval, so HR knows it's their turn
- **Rejection Alert** → Immediately notifies relevant parties if a request is declined
- **Asset Assignment** → Employee is notified when their hardware is ready
- **Welcome Email** → Sent on completion with Employee ID, company email, joining details, and assigned assets

<!-- 📸 SCREENSHOT: Sample welcome email / notification template -->
![Welcome Email Notification](screenshots/welcome-email-notification.png)

---

## The Dashboard

The Onboard360 dashboard gives HR and Management a real-time snapshot of everything happening:

- Pending approvals that need attention
- Employees who've been fully onboarded
- Asset allocation by type
- Department-wise distribution of new hires
- Approval pipeline status at a glance

<!-- 📸 SCREENSHOT: Onboarding Dashboard — full view with all widgets -->
![Onboarding Dashboard](screenshots/onboarding-dashboard.png)

---

## Reports

<!-- 📸 SCREENSHOT: Employee Onboarding Status Report -->
![Onboarding Status Report](screenshots/onboarding-status-report.png)

<!-- 📸 SCREENSHOT: Asset Allocation Report & Department Wise Report -->
![Asset and Department Reports](screenshots/asset-department-reports.png)

---

## Tech Stack

Built entirely on the ServiceNow platform:

- **Service Catalog** — Record Producers, Catalog Items, Catalog Tasks
- **Flow Designer** — End-to-end workflow automation
- **Business Rules** — Auto ID generation, designation filtering, status updates
- **ACLs & Roles** — Secure, role-based data access
- **Notifications** — Event-driven email alerts
- **Scheduled Jobs** — Daily reminders for pending tasks
- **Reports & Dashboards** — Built-in performance analytics

**Application Scope:** `x_company_onboarding`

---

## What's Coming Next

Onboard360 is just getting started. Here's what's on the roadmap:

- **Active Directory Integration** — Auto-sync user accounts with your directory
- **Automated Email Account Creation** — Zero-touch email provisioning
- **CMDB Integration** — Link assets directly to the Configuration Management Database
- **Asset Lifecycle Management** — Track assets from procurement to retirement
- **Service Portal Integration** — A polished self-service portal for employees
- **Virtual Agent Support** — Conversational onboarding assistance
- **IntegrationHub Connectors** — Connect with third-party HR and IT systems

---

## The Bottom Line

Onboard360 turns a fragmented, manual process into something that just works. New hires get a smooth first day. HR stops chasing approvals. IT gets tasks automatically. Managers approve with a single click.

It's not just an automation tool — it's a better first impression for every person who joins your organization.

---

*Built on ServiceNow · Designed for People · Automated for Scale*
