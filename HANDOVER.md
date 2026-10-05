# Handover

## Current version
v0.1.0

## Current phase
Initial specification and first application implementation planning.

## Repository policy
- `main`: stable/approved baseline. Do not modify directly during normal development.
- `develop`: active integration branch.
- Feature branches may be introduced as implementation grows.
- ChatGPT may update `develop` when the user requests development or modification work.
- Direct changes to `main`, destructive operations, production/security changes require explicit confirmation.

## Data safety
Never commit real employee personal information, real application records, passwords, API keys, secrets, or generated production PDFs.

## First target
Overtime application (時間外勤務申請).

## Next work
1. Implement the browser-operable overtime application prototype.
2. Connect applicant -> approval -> return/resubmit -> final approval -> post-approval processing.
3. Add tests and refine UI from user feedback.
4. Keep CHANGELOG and DECISIONS updated with each meaningful change.
