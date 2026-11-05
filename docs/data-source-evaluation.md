# NASA Data Source Evaluation

## 1. Purpose

This document defines how NASA Earth science datasets and APIs will be evaluated and selected for the Earth System Trend Detective project.

## 2. Candidate Data Sources

The following NASA missions and datasets are potential candidates:

| Dataset / Mission | Potential Application |
|---|---|
| MODIS | Land surface and vegetation analysis |
| AIRS | Atmospheric temperature and humidity |
| GPM | Precipitation analysis |
| MERRA-2 | Atmospheric and climate variables |
| GLDAS | Land surface and hydrological variables |
| OMI | Atmospheric composition |

These are candidate sources, not confirmed integrations.

## 3. Evaluation Criteria

Each candidate source must be evaluated based on:

- Data availability and accessibility
- API or download access
- Available variables and measurement units
- Spatial resolution
- Temporal resolution
- Historical data coverage
- Geographic coverage
- Documentation quality
- Usage restrictions and access requirements

## 4. MVP Selection Strategy

The initial MVP will prioritize one verified NASA dataset.

The selected dataset must support:
- A clearly defined scientific variable
- A specific geographic region
- A suitable historical time range
- Time-series generation
- Statistical trend analysis

## 5. Verification Status

Dataset selection is currently pending official resource and API verification.

No candidate dataset should be treated as an implemented integration until its access method and data structure have been tested.

## 6. Final Selection

| Item | Decision |
|---|---|
| Selected dataset | Pending |
| Selected variable | Pending |
| API / access method | Pending |
| Spatial resolution | Pending |
| Temporal resolution | Pending |
| Verification status | Not verified |
## 7. Initial Official Data Access References

| Candidate | Official Reference | Initial Finding |
|---|---|---|
| GPM IMERG | https://gpm.nasa.gov/data/imerg | Multiple temporal resolutions and data formats |
| MERRA-2 | https://gmao.gsfc.nasa.gov/gmao-products/merra-2/data-access_merra-2/ | Long-term atmospheric reanalysis data |
| GLDAS | https://ldas.gsfc.nasa.gov/ldas/get-data | Data access with spatial, temporal and variable subsetting |
| MODIS | https://appeears.earthdatacloud.nasa.gov/ | Candidate for satellite-based land and vegetation data |
| AIRS | https://disc.gsfc.nasa.gov/ | Atmospheric data access through NASA GES DISC |
| OMI | https://disc.gsfc.nasa.gov/ | Atmospheric composition data access through NASA GES DISC |

These references are starting points for investigation.
Their inclusion does not confirm successful API integration.

## 8. Data Access Verification Checklist

Before selecting a dataset, verify:

- [ ] Official dataset identifier and version
- [ ] Required Earthdata account or authentication
- [ ] Programmatic API or download method
- [ ] Ability to select a geographic region
- [ ] Ability to select a date range
- [ ] Available variables and units
- [ ] Temporal and spatial resolution
- [ ] Sample data successfully retrieved
- [ ] Data can be processed using Python
- [ ] Data license, usage restrictions and attribution requirements

## 9. Current Decision

No dataset has been selected yet.

The final MVP dataset will be selected after testing official access methods and confirming that the data supports the project's analysis workflow.
