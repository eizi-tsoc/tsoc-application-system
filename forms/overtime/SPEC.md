# 時間外勤務申請 - Specification v0.2

Form code: OVERTIME

## Source form
The first web form is based on the existing TSOC 時間外勤務申請書.

## Applicant section
Auto-populate from employee master:
- employee ID
- name
- department

## Application date
- 届出年月日は職員が入力しない。
- 下書き作成日ではなく、正式に「申請する」を実行した日をシステムが自動記録する。
- 差戻し後の再申請では当初の届出年月日を保持し、再申請日時は履歴として別途記録する。

## Work schedule / 所定勤務時間
- 管理画面で部門ごとに基本勤務時間・シフト（勤務パターン）を登録する。
- 申請者は勤務日を指定したうえで「当日のシフト」を選択する。
- シフト候補は申請者の所属部門に登録された有効なシフトだけを表示する。全部門のシフトは表示しない。
- シフトを選択すると、所定勤務の開始時刻・終了時刻・所定休憩時間を自動表示する。
- 選択したシフトIDと、その時点の名称・開始/終了・休憩時間を申請データにスナップショットして履歴を保持する。
- 将来、日別シフト連携が実装された場合は当日の予定シフトを初期選択できるが、所属部門で絞り込む原則は維持する。

## Input
- overtime work date
- today's shift (department-filtered selection)
- scheduled start/end/break (automatic from selected shift)
- overtime start
- overtime end
- calculated overtime duration
- reason overtime is necessary
- overtime reduction effort
- break yes/no and time
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
