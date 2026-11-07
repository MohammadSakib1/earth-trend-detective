# Backend Project Structure

## 1. Purpose

This document defines the proposed backend directory structure for the Earth System Trend Detective application.

The backend will use Python and FastAPI.

## 2. Proposed Directory Structure

```text
backend/
├── app/
│   ├── main.py
│   ├── api/
│   │   ├── routes/
│   │   │   ├── health.py
│   │   │   ├── variables.py
│   │   │   └── analysis.py
│   │   └── schemas/
│   │       ├── analysis_request.py
│   │       └── analysis_response.py
│   ├── core/
│   │   ├── config.py
│   │   └── exceptions.py
│   ├── services/
│   │   ├── analysis_service.py
│   │   └── metadata_service.py
│   ├── data/
│   │   ├── adapters/
│   │   │   ├── base.py
│   │   │   └── merra2_adapter.py
│   │   └── processing/
│   │       ├── validation.py
│   │       └── time_series.py
│   ├── analysis/
│   │   ├── descriptive.py
│   │   ├── trend.py
│   │   └── significance.py
│   └── storage/
│       └── results_repository.py
├── tests/
│   ├── unit/
│   ├── integration/
│   └── fixtures/
├── requirements.txt
├── .env.example
└── README.md
```

## 3. Module Responsibilities

| Module | Responsibility |
|---|---|
| main.py | Initializes the FastAPI application |
| api/routes | Defines REST API endpoints |
| api/schemas | Validates request and response structures |
| core | Configuration and shared exceptions |
| services | Coordinates application workflows |
| data/adapters | Retrieves data from NASA sources |
| data/processing | Standardizes and validates data |
| analysis | Performs statistical analysis |
| storage | Stores analysis results and metadata |
| tests | Contains automated tests |

## 4. Architectural Rules

- Keep the backend organized by responsibility.
- Keep NASA-specific logic inside data adapters.
- Keep statistical calculations separate from API routes.
- Validate incoming requests using schemas.
- Avoid placing all application logic inside main.py.
- Use configuration files and environment variables for settings.
- Keep the design modular while maintaining a simple MVP.

## 5. Initial Technology Choices

| Technology | Purpose |
|---|---|
| Python | Backend language |
| FastAPI | REST API framework |
| Pydantic | Request and response validation |
| NumPy | Numerical computation |
| Pandas | Data processing |
| SciPy | Statistical analysis |
| pytest | Backend testing |

These choices may be refined during implementation.

## 6. Current Status

| Component | Status |
|---|---|
| Backend structure | Proposed |
| Python implementation | Not started |
| API implementation | Not started |
| NASA adapter implementation | Not started |
| Automated tests | Not started |
