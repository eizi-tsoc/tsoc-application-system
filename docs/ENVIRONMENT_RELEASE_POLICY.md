# Environment and Release Policy

Status: Adopted
Date: 2026-10-05

## Purpose
TSOC Staff System is developed and operated with separate test and production environments using the same application architecture.

## Source and environments
- GitHub repository remains Private and is the source of truth.
- `develop` is the source branch for the test environment.
- `main` is the approved source branch for the production environment.
- Test and production use the same application architecture and configuration model, but separate data, credentials, secrets, URLs and external-service settings.

## Standard release flow
1. Implement new forms, features and fixes on `develop`.
2. Deploy `develop` to the test environment.
3. Perform browser-based functional testing.
4. Record defects and corrections.
5. Obtain operational confirmation.
6. Promote the confirmed version to `main`.
7. Deploy `main` to production.
8. Record release version and release history.

Production must not normally be edited directly.

## Version management
Use semantic versions:
- MAJOR: incompatible or major system changes.
- MINOR: new forms or backward-compatible features.
- PATCH: bug fixes and minor corrections.

Always record:
- current test version
- current production version
- release date
- changes
- known issues
- rollback target

## Error / incident history
For each meaningful defect or incident record:
- occurrence date/time
- environment
- application version
- affected function/form
- symptom
- cause
- corrective action
- verification result
- fixed version
- production release date if applicable

Major defects should also be tracked with a GitHub Issue.

## Rollback
Every production release must identify the previous known-good version. If a critical production defect occurs, restore the last known-good version while the correction is tested on the test environment.

## Data separation
Never use real production employee/application data in source control.
Test and production data stores must be separate.
Test data should be synthetic unless explicitly approved and protected.

## Access control
Both test and production applications require authentication before application content is accessible.
Authorization is role/permission based. A logged-in employee may hold multiple permissions without switching accounts.
Direct URL access to protected screens must require authentication and authorization.

## Deployment platform requirements
The selected platform must support:
- deployment from a Private GitHub repository
- separate test and production services/environments
- branch-based deployment
- environment variables/secrets
- HTTPS
- application authentication
- persistent database connectivity
- deployment history and logs
- rollback/redeploy capability
- future PDF generation and email delivery

## Initial platform direction
For the first hosted implementation, evaluate a managed application platform rather than GitHub Pages. The platform must support the full application, not only static HTML.
