# TSOC Application System

Internal web application for TSOC staff applications, approval workflows, document generation and related employee-master workflows.

## Status
Current development version: **v0.2.0**  
Phase: browser prototype for the first application.

## Branches
- `main`: stable/approved baseline
- `develop`: active development

Normal development is performed on `develop`. Direct changes to `main` require explicit confirmation.

## First target
**時間外勤務申請 (Overtime Application)**

Flow target:

`Draft -> Submit -> Approval -> Return/Resubmit or Reject -> Final Approval -> PDF -> Post-approval processing -> Complete`

## Browser prototype
A dependency-free UI/flow prototype is available under `prototype/`.

Current prototype supports overtime input, automatic duration calculation, local draft save, submit simulation, approval preview and approve/return/reject demo actions.

It is not yet a production system: backend, authentication, database, email, PDF generation and hosted deployment remain to be implemented.

## Documentation
- `docs/REQUIREMENTS.md`
- `docs/DATABASE.md`
- `docs/WORKFLOW.md`
- `docs/DECISIONS.md`
- `CHANGELOG.md`
- `HANDOVER.md`
- `forms/overtime/SPEC.md`
- `prototype/README.md`

## Security rule
Do not commit real employee personal information, real application records, credentials, API keys, secrets, or production-generated PDFs to this repository.
