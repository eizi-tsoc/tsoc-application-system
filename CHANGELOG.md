# Changelog

All notable changes to TSOC Application System are recorded here.

## [0.2.1] - 2026-10-05
### Changed
- 届出年月日を正式提出時の自動記録として明確化。
- 所定勤務時間を、所属部門で絞り込んだ当日シフト選択方式へ変更。
- 選択シフトから所定開始・終了・休憩時間を自動表示するプロトタイプへ更新。
- 選択した勤務パターンと所定時間を申請時点でスナップショットする設計を追加。

## [0.2.0] - 2026-10-05
### Added
- First browser-operable overtime application prototype.
- Applicant input screen with sample employee/department data.
- Automatic overtime duration calculation.
- Browser-local draft save.
- Submit simulation and approval detail screen.
- Approve, return and reject demo actions.
- Mandatory comment validation for return/reject.

### Limitations
- Prototype only: no backend, authentication, database, email, PDF generation or deployment yet.
- Data is stored only in browser localStorage for UI testing.

## [0.1.0] - 2026-10-05
### Added
- Initial project governance and handover documents.
- Initial requirements and decision log.
- Overtime application v0.1 specification.
- Development branch workflow.
