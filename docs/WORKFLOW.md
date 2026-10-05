# Workflow v0.1

## Overtime application
DRAFT -> SUBMITTED -> IN_APPROVAL

Each sequential approval step supports:
- APPROVE
- RETURN (comment required)
- REJECT (comment required)

RETURN -> applicant edits -> RESUBMITTED -> approval resumes according to the defined workflow policy.

Final approval:
IN_APPROVAL -> APPROVED -> official PDF finalized -> post-approval task created.

Post-approval:
APPROVED -> processing PENDING/PROCESSING -> COMPLETED.

## Approval configuration
Initial UI supports one approver per step.

Approver types:
- EMPLOYEE: fixed employee
- APPLICANT_MANAGER: dynamic applicant manager

Future-compatible types may include ROLE, DEPARTMENT, POSITION and PERMISSION.

## Route resolution
A workflow routing rule selects a workflow using the form plus applicant context such as department/site. At submission, dynamic resolvers are converted to actual employee IDs and copied to application workflow steps. Later master changes do not silently mutate the in-flight route.

## Overtime example
STEP 1: fixed employee
STEP 2: fixed employee
STEP 3: applicant's manager (final approval)
Then: timekeeping/payroll processing destination.
