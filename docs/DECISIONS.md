# Decision Log

## D-001
Use a common application engine rather than independent systems for each application form.

## D-002
One employee login can hold multiple permissions; no account switching is required for applicant/approver roles.

## D-003
A returned application can be corrected and resubmitted.

## D-004
Final approval generates/finalizes the official PDF.

## D-005
Employee ID is linked to employee email for workflow notifications.

## D-006
Employee is the system business identity. Employment status, permissions and login availability are tied to the employee record; retired employee history remains.

## D-007
Once formally submitted, an application is not physically deleted.

## D-008
Return/resubmission uses the same application number and retains revisions.

## D-009
Approval routes are separated from form definitions.

## D-010
Approvers may be fixed employees or dynamic resolvers. Initial implementation uses one approver per sequential step; data design remains extensible.

## D-011
The actual approval route is resolved and frozen at submission time.

## D-012
Retirement processing checks unresolved own applications and assigned approvals.

## D-013
Administrators may explicitly reassign/handover workflow items with reason and audit history.

## D-014
Employee email is used for application status notifications.

## D-015
Fixed and dynamic approver types may coexist in one route.

## D-016
Final approval and post-approval clerical processing are separate stages.

## D-017
Each form may configure its own post-approval processing/notification destination.

## D-018
Final approval finalizes the official PDF; post-processing state is separate.

## D-019
Initial version uses one main processing destination; data design remains extensible.

## D-020
Form definitions and approval routes remain separate.

## D-021
Applicable workflow can be selected automatically from applicant/form/organization conditions.

## D-022
Fixed employee and dynamic approver (e.g. applicant's manager) may be mixed in workflow steps.

## D-023
Workflow configuration is validated before activation.

## D-024
Administration will provide a workflow-route test/preview for a selected employee and form.

## D-025
Post-approval processing should support functional groups such as payroll/timekeeping rather than hard-coding an individual.

## D-026
Organizational position and system/business responsibility are separate concepts; an employee may hold multiple responsibilities.

## D-027
Workflow definitions are versioned so changes do not rewrite historical applications.

## D-028
GitHub is the source of truth for source code, specifications, decisions, changelog and handover. Real operational/personal data stays outside GitHub.

## D-029
Normal requested development work may be written directly to `develop`. Direct `main` changes, destructive actions and production/security-sensitive changes require explicit user confirmation.

## D-030
届出年月日は正式提出時にシステムが自動記録する。下書き作成日は届出年月日にしない。差戻し後も当初届出年月日は保持し、再申請日時を履歴として記録する。

## D-031
所定勤務時間は自由入力を基本とせず、部門ごとに管理する勤務パターン（シフト）から申請者が当日のシフトを選択する。

## D-032
時間外勤務申請で表示するシフト候補は、勤務日時点の申請者所属部門に絞り込む。全部門のシフト候補は表示しない。

## D-033
選択したシフトから所定開始・終了・休憩時間を自動設定し、申請時点の値をスナップショットとして保存する。

## D-034
当面のブランチ運用は `develop` と `main` の2本を基本とする。`develop` は開発・テスト確認用の最新版、`main` は確認済みの本番リリース候補ソースとする。GitHubブランチと実行環境は別物であり、develop→テスト環境、main→本番環境という対応を基本とする。
