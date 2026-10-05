# Requirements v0.1

## Goal
Replace direct editing of internal Word application forms with a reusable web-based application, approval, document and employee-information platform.

## Core principles
- One common application engine; do not build a separate system per form.
- Employee is the business identity. Do not maintain a duplicate business user ledger.
- One login can expose applicant, approver, processing and administrative permissions.
- Employee ID is linked to email for workflow notifications.
- Submitted applications are retained for audit; drafts may be deleted.
- Returned applications keep the same application number and are resubmitted with revision history.
- Rejection is terminal. Return allows correction and resubmission.
- Approval routes are configurable and separate from form definitions.
- Approval route is resolved and frozen at submission time.
- Final approval finalizes the formal document/PDF.
- Post-approval clerical processing is tracked separately from approval.
- Historical application snapshots must not change when current employee master data changes.

## Initial application
時間外勤務申請 (Overtime Application)

Fields derived from the existing TSOC form:
- application date
- department
- applicant name
- overtime work date
- start time
- end time
- overtime duration
- reason overtime is necessary
- effort to reduce overtime
- break: yes/no and time
- planned late-night work: yes/no

The current paper/Word form states that overtime should be applied for in advance and that the reason should be concrete and hours limited to the necessary range.

## Initial workflow statuses
DRAFT, SUBMITTED, IN_APPROVAL, RETURNED, RESUBMITTED, REJECTED, APPROVED, COMPLETED, WITHDRAWN, CANCELLED.

## Notifications
Email notifications are event-based. Recipient email is snapshotted at send time for audit.

## Out of repository
Real employee data, production application data, secrets, passwords, API keys and production PDFs must not be stored in GitHub.
