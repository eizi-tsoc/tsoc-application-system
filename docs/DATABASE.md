# Database Concept v0.1

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
- work_patterns
- employee_work_patterns
- work_shifts

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
- Dynamic approval routes resolve to actual employees at submission.
- Submitted applications are retained.
- Return/resubmission retains revision history.
- Employee and organization changes are effective-dated where history matters.
