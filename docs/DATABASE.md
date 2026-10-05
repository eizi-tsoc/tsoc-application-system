# Database Concept v0.2

This is a conceptual model; implementation technology is not yet fixed.

## Employee / organization
- employees
- employee_addresses (effective dated; source_application_id)
- departments
- positions
- job_types
- employee_assignments (effective dated)
- responsibility_groups / employee_responsibilities

## Work schedules
### work_patterns
Department-scoped shift/master patterns.
- id
- department_id
- pattern_code
- pattern_name
- scheduled_start
- scheduled_end
- scheduled_break_minutes
- active
- display_order

### employee_work_patterns
Optional employee-specific eligibility/default relationship for future use.

### work_shifts
Optional date-specific employee shift assignment for future roster integration.
- employee_id
- work_date
- work_pattern_id
- scheduled_start
- scheduled_end
- scheduled_break_minutes

### Overtime selection rule
1. Determine applicant's primary department on the overtime work date.
2. Load only active work_patterns belonging to that department.
3. Applicant selects the actual shift for that day.
4. Selected pattern automatically fills scheduled start/end/break.
5. Application stores both work_pattern_id and a snapshot of the selected schedule so later master edits do not rewrite history.

## Form definitions
- form_definitions
- form_versions
- form_fields

## Applications
- applications
- application_snapshots
- application_data
- application_revisions

## Workflow
- workflow_definitions
- workflow_versions
- workflow_routing_rules
- workflow_steps
- workflow_step_approvers
- application_workflow_steps
- application_approval_actions

## Post approval
- post_approval_definitions
- post_approval_tasks

## Documents / notifications / audit
- documents
- notifications
- audit_logs

## Key rules
- Historical applicant identity/organization is snapshotted.
- Selected work pattern and scheduled hours are snapshotted on the application.
- Dynamic approval routes resolve to actual employees at submission.
- Submitted applications are retained.
- Return/resubmission retains revision history.
- Employee and organization changes are effective-dated where history matters.
