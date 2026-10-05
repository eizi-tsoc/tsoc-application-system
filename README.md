# TSOC Application System

Internal web application for TSOC staff applications, approval workflows, document generation and related employee-master workflows.

## Status
Current version: **v0.1.0**  
Phase: specification baseline / overtime application prototype planning.

## Branches
- `main`: stable/approved baseline
- `develop`: active development

Normal development is performed on `develop`. Direct changes to `main` require explicit confirmation.

## First target
**時間外勤務申請 (Overtime Application)**

Planned flow:

`Draft -> Submit -> Approval -> Return/Resubmit or Reject -> Final Approval -> PDF -> Post-approval processing -> Complete`

## Documentation
- `docs/REQUIREMENTS.md`
- `docs/DATABASE.md`
- `docs/WORKFLOW.md`
- `docs/DECISIONS.md`
- `CHANGELOG.md`
- `HANDOVER.md`
- `forms/overtime/SPEC.md`

## Security rule
Do not commit real employee personal information, real application records, credentials, API keys, secrets, or production-generated PDFs to this repository.
