# Earth System Trend Detective 🌍

**NASA Space Apps Challenge 2026 — Earth System Trend Detective**

An interactive web application designed to explore environmental changes over time using Earth science data and statistical trend analysis.

## 1. Project Overview

Earth's systems are constantly changing. Understanding these changes requires analyzing scientific observations across different geographic regions and time periods.

**Earth System Trend Detective** aims to help users explore environmental trends by selecting scientific variables, geographic regions, and time ranges. The application will process Earth science data, perform statistical analysis, and present the results through interactive visualizations.

The project emphasizes scientific transparency by presenting data sources, quality information, uncertainty, and analytical limitations.

## 2. Project Objectives

- Explore changes in Earth system variables over time.
- Support geographic and temporal data selection.
- Retrieve and process data from NASA Earth science sources.
- Generate time-series visualizations.
- Estimate trends using statistical methods.
- Evaluate statistical significance.
- Communicate uncertainty and data limitations.

## 3. Planned Core Features

| Feature | Description |
|---|---|
| Variable Selection | Select an Earth science variable |
| Geographic Selection | Define an area of interest |
| Time Range Selection | Choose the analysis period |
| NASA Data Integration | Retrieve data from a verified NASA source |
| Data Validation | Check data quality and missing values |
| Time-Series Analysis | Generate time-series data |
| Trend Estimation | Estimate environmental trends |
| Statistical Testing | Evaluate trend significance |
| Interactive Visualization | Display charts and summaries |
| Data Provenance | Show dataset information and methodology |

## 4. System Architecture

The application is planned as a modular monolith with separate frontend and backend responsibilities.

### Technology Stack

| Layer | Technology |
|---|---|
| Frontend | React, TypeScript |
| Backend | Python, FastAPI |
| Data Processing | Pandas, NumPy |
| Statistical Analysis | SciPy |
| Visualization | Interactive charting library (to be finalized) |
| Testing | pytest and frontend testing tools |

### High-Level Workflow

1. User selects a variable, geographic region, and time period.
2. Backend validates the analysis request.
3. NASA data adapter retrieves the selected dataset.
4. Data processing standardizes and validates the retrieved data.
5. Statistical modules perform trend analysis.
6. Backend returns analysis results and metadata.
7. Frontend displays charts, summaries, and data quality information.

## 5. Statistical Analysis

The planned analysis methods include:

- Descriptive statistics
- Linear regression
- Sen's slope estimation
- Mann-Kendall trend test
- Statistical significance evaluation

The application will communicate statistical results carefully and will not interpret correlation as causation.

## 6. Scientific Data Sources

Potential NASA data sources under evaluation include:

- GPM IMERG
- MERRA-2
- GLDAS
- MODIS
- AIRS
- OMI

**Note:** These are candidate sources, not confirmed integrations. The initial MVP will prioritize one dataset after programmatic retrieval and processing have been verified.

## 7. Project Documentation

Technical documentation is maintained in the [`docs/`](./docs/) directory.

| Document | Description |
|---|---|
| [Requirements](./docs/requirements.md) | Functional and non-functional requirements |
| [Architecture](./docs/architecture.md) | System architecture and API design |
| [Data Source Evaluation](./docs/data-source-evaluation.md) | Candidate NASA datasets and evaluation criteria |
| [Data Pipeline](./docs/data-pipeline.md) | Data retrieval and processing workflow |
| [Data Processing & Validation](./docs/data-processing-validation.md) | Standardization and quality checks |
| [Statistical Analysis Design](./docs/statistical-analysis-design.md) | Statistical methods and interpretation |
| [UI/UX Design](./docs/ui-ux-design.md) | Interface design and user experience |
| [Backend Project Structure](./docs/backend-project-structure.md) | Proposed backend organization |
| [Frontend Wireframes](./docs/wireframes.md) | Proposed interface layouts |
| [Implementation Roadmap](./docs/implementation-roadmap.md) | Development phases and priorities |

## 8. Development Status

**Current stage: System Design and Documentation**

| Component | Status |
|---|---|
| Project requirements | Documented |
| System architecture | Documented |
| Data pipeline design | Documented |
| Statistical analysis design | Documented |
| UI/UX design | Documented |
| Backend structure | Proposed |
| Frontend wireframes | Proposed |
| Implementation roadmap | Documented |
| Backend implementation | Not started |
| Frontend implementation | Not started |
| NASA data integration | Not verified |
| End-to-end testing | Not started |
| Deployment | Not started |

## 9. Future Development

Planned development priorities:

1. Establish the backend and frontend foundations.
2. Verify and integrate one NASA dataset.
3. Implement data processing and validation.
4. Implement statistical analysis modules.
5. Build interactive visualizations.
6. Integrate frontend and backend.
7. Test and deploy the MVP.

## 10. Team

**Project:** Earth System Trend Detective  
**Challenge:** NASA Space Apps Challenge 2026  
**Team Size:** 4 members

## 11. Repository

GitHub: [MohammadSakib1/earth-trend-detective](https://github.com/MohammadSakib1/earth-trend-detective)

---

*Built for NASA Space Apps Challenge 2026.*

