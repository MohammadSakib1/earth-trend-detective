# Contributing Guidelines

Thank you for contributing to Earth System Trend Detective!

This document defines the basic collaboration and development guidelines for the project team.

## 1. Team Collaboration

- All team members should communicate before making major architectural changes.
- Each member should work on assigned tasks.
- Keep the team informed about progress and blockers.
- Review important changes before merging them into the main branch.

## 2. Branching Strategy

The project uses the following branch structure:

| Branch | Purpose |
|---|---|
| `main` | Stable project version |
| `develop` | Integration of ongoing development |
| `feature/*` | New features |
| `fix/*` | Bug fixes |
| `docs/*` | Documentation updates |

Example branch names:

- `feature/backend-api`
- `feature/frontend-dashboard`
- `feature/nasa-data-adapter`
- `docs/update-readme`

## 3. Commit Guidelines

Use clear and meaningful commit messages.

Examples:

- `Add backend health endpoint`
- `Implement NASA data adapter`
- `Create time-series visualization`
- `Update statistical analysis documentation`
- `Fix data validation logic`

Avoid unclear messages such as `update`, `changes`, or `final work`.

## 4. Pull Request Guidelines

Before merging changes:

1. Explain what was changed.
2. Describe the purpose of the changes.
3. Check for errors and unintended modifications.
4. Ensure related documentation is updated.
5. Request review from another team member when appropriate.

## 5. Code Quality

- Keep functions and modules focused on specific responsibilities.
- Avoid unnecessary code duplication.
- Use meaningful variable and function names.
- Keep NASA-specific retrieval logic inside data adapters.
- Keep statistical calculations separate from API routes.
- Add tests for important functionality.

## 6. Documentation Guidelines

- Update relevant documentation when architecture or functionality changes.
- Do not mark planned features as implemented.
- Record dataset sources and versions.
- Document known limitations and assumptions.
- Keep README and technical documentation consistent.

## 7. Security Guidelines

- Never commit passwords, API keys, tokens, or private credentials.
- Store local secrets in `.env`.
- Use `.env.example` to document required configuration.
- Keep `.env` excluded through `.gitignore`.

## 8. Scientific Integrity

- Use verified scientific data sources.
- Clearly identify synthetic data used for testing.
- Do not invent or alter scientific results.
- Report missing data and uncertainty transparently.
- Do not interpret statistical association as causation.

## 9. Development Workflow

1. Select an assigned task.
2. Create an appropriate branch.
3. Implement the changes.
4. Test the changes.
5. Commit with a meaningful message.
6. Open a pull request.
7. Review and merge approved changes.

Thank you for helping build Earth System Trend Detective!
