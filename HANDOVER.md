# Handover

## Current version
v0.2.0

## Current phase
Browser-operable overtime application prototype implemented on `develop`.

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

## Current limitations
There is no backend, database, login/authentication, email notification, PDF generation, audit persistence or hosted test environment yet.

## Next work
1. User UI/flow review of the overtime prototype.
2. Select the implementation/deployment stack for a real test environment.
3. Implement employee/auth foundation and persistent application storage.
4. Implement frozen workflow resolution and approval action history.
5. Implement PDF generation and post-approval processing.
6. Keep CHANGELOG, DECISIONS and this HANDOVER updated with each meaningful change.
