# myr-army Project Guidelines

## Token Optimization
Be concise. Skip preamble, summaries, and closing remarks unless asked. Show code directly.

## Stack Overview
- Backend: Python (FastAPI), Java (Spring Boot), Go
- Cloud: AWS, GCP
- Database: PostgreSQL, Cloud SQL
- CI/CD: GitLab (repos + pipelines)

## Code Style
- Write clean, idiomatic code for each language
- Prefer explicit over implicit
- Error handling at system boundaries only — let internal errors propagate
- **Minimal comments**: only add comments when the code or resource is genuinely non-obvious and would confuse a maintainer without explanation. No boilerplate, no "this function does X" restating the obvious
- Favor simplicity and readability over cleverness

## Security Baseline
- Secrets never hardcoded — environment variables or secret managers (Secrets Manager, Secret Manager, Vault)
- All inputs validated at system boundaries (API endpoints, CLI args, external data)
- Dependencies pinned and scanned; no known-vulnerable versions
- Least-privilege for IAM roles, DB grants, and service accounts
- TLS everywhere in production; no plain HTTP

## Maintainability Principles
- Prefer the simplest solution that works — avoid premature abstraction
- Small, focused modules/packages/classes — single responsibility
- No dead code; remove unused imports, functions, variables
- Consistent naming conventions per language idioms
- Every change must be easy to review: small diffs, one concern per commit

## Architecture Principles
- Design for horizontal scalability
- Prefer managed cloud services over self-hosted where sensible
- 12-factor app principles apply
- Stateless services by default; externalize state to databases/caches

## Conventions
- REST APIs follow OpenAPI 3.x spec
- Database migrations are versioned (Flyway / Alembic)
- All infrastructure changes go through IaC (Terraform preferred)
- Container images are minimal (multi-stage, non-root, distroless/alpine)

## Task Completion

Whenever an agent answers a question, finishes a task or has follow-up questions to ask the user, use the AskQuestions tool to gather more information. Always do this before ending the task. This allows you to clarify any uncertainties and ensure that you have all the necessary information to complete the task effectively. Only end the task when the user has no more questions or can confirm that the task is complete. Always prompt the user to ask any follow-up questions they may have before ending the task. This will help ensure that the user is satisfied with the outcome and that all their concerns have been addressed.