# System Architecture — Earth System Trend Detective

## 1. Introduction

### 1.1 Purpose

This document describes the proposed software architecture of the Earth System Trend Detective platform.

It defines the major system components, their responsibilities, interactions, and the overall data-processing workflow.

The architecture will guide the development and integration of the frontend, backend, NASA data access, and scientific analysis modules.

### 1.2 Architecture Goals

The architecture aims to:

- Provide a modular and maintainable application structure.
- Support integration with verified NASA Earth science data sources.
- Separate data retrieval, processing, statistical analysis, and visualization.
- Ensure scientific transparency and traceability.
- Support future expansion to additional variables, regions, and datasets.

## 2. Proposed Architecture Style

The initial application will follow a **Modular Monolith Architecture**.

The application will be organized into logically separated modules within a single backend application.

### Reasons for This Choice

- Easier development and deployment for a small team.
- Clear separation of responsibilities.
- Simpler integration and testing.
- Ability to extend individual modules without redesigning the entire system.
- Avoidance of unnecessary microservice infrastructure during the initial development phase.

## 3. Technology Direction

The proposed technology stack is:

| Layer | Proposed Technology | Responsibility |
|---|---|---|
| Frontend | React | User interface and dashboard |
| Frontend Language | TypeScript | Type-safe application development |
| Backend | Python | Application logic and data processing |
| Backend Framework | FastAPI | REST API and request handling |
| Data Analysis | Python scientific libraries | Time-series and statistical analysis |
| Visualization | Charting library (to be selected) | Trend charts |
| Version Control | Git and GitHub | Collaboration and source management |

Final technology and library choices may be adjusted during implementation.

## 4. Major System Components

### 4.1 Frontend Layer

Responsible for user interaction and result presentation.

Responsibilities:
- Variable selection
- Geographic region selection
- Time-period selection
- Submission of analysis requests
- Display of time-series charts
- Presentation of trend summaries and statistical results

### 4.2 Backend API Layer

Responsible for receiving and coordinating application requests.

Responsibilities:
- Receive frontend requests
- Validate user inputs
- Coordinate data retrieval and analysis
- Handle application errors
- Return structured responses

### 4.3 Variable Catalog

Maintains information about supported Earth science variables.

Responsibilities:
- Store variable identifiers and names
- Provide descriptions and measurement units
- Identify associated datasets
- Describe temporal and spatial coverage
- Define supported aggregation options

### 4.4 NASA Data Adapter

Responsible for communication with external Earth science data sources.

Responsibilities:
- Retrieve data from configured sources
- Convert source-specific responses into a common internal format
- Handle retrieval errors
- Preserve relevant dataset metadata

The final NASA data source and access method will be selected after dataset evaluation.

### 4.5 Data Processing Module

Responsible for preparing retrieved data for analysis.

Responsibilities:
- Validate observations
- Check missing values
- Handle invalid observations using documented rules
- Verify dates and measurement units
- Generate analysis-ready time-series data

### 4.6 Statistical Analysis Engine

Responsible for identifying and evaluating temporal trends.

Responsibilities:
- Estimate trend direction
- Calculate the rate of change
- Perform an appropriate statistical significance test
- Report relevant statistical evidence and uncertainty

### 4.7 Result and Provenance Module

Responsible for preparing the final analysis output.

Responsibilities:
- Combine analysis results and metadata
- Include dataset and source information
- Include analysis methodology
- Communicate uncertainty and limitations
- Prepare structured responses for the frontend

## 5. Architectural Design Principles

The system will follow these principles:

1. Separation of Concerns: Each component will have a clearly defined responsibility.
2. Modularity: Components should be independently maintainable where possible.
3. Data Transparency: Every scientific result should be linked to its data source.
4. Scientific Integrity: No fabricated observations or unsupported conclusions.
5. Extensibility: Additional datasets and variables should be supported through modular integration.
6. Testability: Processing and analysis components should be independently testable.

## 6. Initial Architecture Status

This architecture is a preliminary design.

The following decisions remain open:

- Final NASA dataset and data access method
- Supported variables and geographic regions
- Spatial and temporal resolution
- Data processing and aggregation rules
- Final statistical methodology
- Deployment infrastructure

These decisions will be updated after data-source evaluation and technical validation.

## 7. High-Level Architecture Diagram

```mermaid
flowchart TB
    USER["User"]

    subgraph FRONTEND["Frontend Layer"]
        UI["React Dashboard"]
        INPUT["Variable, Region and Time Selection"]
        CHART["Time-Series Charts"]
        DISPLAY["Trend Summary and Results"]
        UI --> INPUT
        CHART --> UI
        DISPLAY --> UI
    end

    subgraph BACKEND["Backend Layer - FastAPI"]
        API["REST API"]
        VALIDATE["Request Validation"]
        CATALOG["Variable Catalog"]
        ADAPTER["NASA Data Adapter"]
        PROCESS["Data Processing"]
        ANALYSIS["Statistical Analysis Engine"]
        RESULT["Result Builder"]
        PROVENANCE["Data Provenance"]
    end

    NASA["NASA Earth Science Data Sources"]

    USER --> UI
    INPUT -->|"Analysis Request"| API
    API --> VALIDATE
    VALIDATE --> CATALOG
    CATALOG --> ADAPTER
    ADAPTER <-->|"Data Retrieval"| NASA
    ADAPTER --> PROCESS
    PROCESS --> ANALYSIS
    ANALYSIS --> RESULT
    RESULT --> PROVENANCE
    PROVENANCE --> API
    API -->|"Analysis Response"| CHART
    API --> DISPLAY
