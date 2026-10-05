# 時間外勤務申請 - Specification v0.1

Form code: OVERTIME

## Source form
The first web form is based on the existing TSOC 時間外勤務申請書.

## Applicant section
Auto-populate from employee master:
- employee ID
- name
- department
- relevant work pattern/shift where available

## Input
- overtime work date
- scheduled start/end (auto where available)
- overtime start
- overtime end
- calculated overtime duration
- reason overtime is necessary
- overtime reduction effort
- break yes/no
- break time/duration
- planned late-night work yes/no

## Actions
- Save draft
- Submit
- Withdraw where policy permits
- Edit and resubmit after return

## Applicant visibility
Before submission show the resolved approval route preview.
After submission show application number, status and progress timeline.

## Approval
Sequential steps. Initial implementation: one approver per step.
Approver can APPROVE, RETURN or REJECT.
RETURN and REJECT require a comment.

## Final approval
- freeze/finalize formal application data
- generate official PDF
- record final approval timestamp
- create configured post-approval task

## Post-approval
Initial overtime destination: timekeeping/payroll processing role/group.
The application can display e.g. 最終承認済 / 勤怠処理中 until processing completion.

## PDF
Web UI does not need to visually mimic the Word form. Final PDF should preserve the formal content and may add application number, approval history and final approval timestamp.
