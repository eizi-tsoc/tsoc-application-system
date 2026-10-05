# Handover

## Current version
v0.2.1

## Current phase
Overtime prototype updated with department-filtered shift selection on `develop`.

## Repository policy
- `main`: stable/approved baseline. Do not modify directly during normal development.
- `develop`: active integration branch.
- Feature branches may be introduced as implementation grows.
- ChatGPT may update `develop` when the user requests development or modification work.
- Direct changes to `main`, destructive operations, production/security changes require explicit confirmation.

## Data safety
Never commit real employee personal information, real application records, passwords, API keys, secrets, or generated production PDFs.

## Implemented in v0.2.0
- `prototype/index.html`: overtime applicant + approval screens.
- `prototype/styles.css`: responsive UI.
- `prototype/app.js`: duration calculation, local draft, submit simulation, approval/return/reject demo.
- `prototype/README.md`: test instructions.

## Implemented in v0.2.1
- 届出年月日は正式提出時に自動記録する仕様。
- 部門ごとに基本勤務時間・シフトを管理する設計。
- 申請時の当日シフト候補は所属部門だけに絞り込み。
- 選択シフトから所定開始・終了・休憩時間を自動表示。
- 選択シフト情報は申請時点でスナップショット保存する設計。

## Current limitations
There is no backend, database, login/authentication, email notification, PDF generation, audit persistence or hosted test environment yet.

## Next work
1. User UI/flow review of the overtime prototype.
2. Select the implementation/deployment stack for a real test environment.
3. Implement employee/auth foundation and persistent application storage.
4. Implement frozen workflow resolution and approval action history.
5. Implement PDF generation and post-approval processing.
6. Keep CHANGELOG, DECISIONS and this HANDOVER updated with each meaningful change.
