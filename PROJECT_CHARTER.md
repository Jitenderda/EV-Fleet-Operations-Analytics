# Project Charter

## Working title

EV Fleet Operations Analytics

## Problem statement

EV fleet managers need reliable analysis of vehicle usage, battery health, charging performance and maintenance activity to improve fleet availability and reduce operating costs.

## Primary user

The primary user is an EV fleet or operations manager.

## Main business questions

1. Which vehicles are being utilized efficiently?
2. Which vehicles consume unusually high energy per kilometre?
3. Which charging stations have low utilization or high failure rates?
4. Which vehicles show signs of battery-health risk?
5. Which vehicles have the highest maintenance cost or downtime?
6. Are enough vehicles available and charged for upcoming operations?

## Planned data domains

- Vehicle information
- GPS and trip summaries
- Charging sessions
- Battery-health snapshots
- Charging stations
- Maintenance events

## Version 1 deliverables

- Clean and documented datasets
- SQL analysis
- Python exploratory-analysis notebook
- Power BI dashboard
- Data dictionary
- Business findings and recommendations
- Project limitations and assumptions

## Version 1 scope

Version 1 will focus on batch analysis for data-analyst skills.

Real-time IoT ingestion, physical hardware, predictive maintenance, RAG and AI agents are optional future extensions.

## Definition of done

Version 1 is complete when:

- The data model is documented
- Data-quality checks are completed
- SQL analysis is reproducible
- Python EDA is completed
- The dashboard answers the main business questions
- Findings are validated
- Recommendations are clearly documented
- The project can be explained in an interview

## Privacy rule

Only public, synthetic or anonymized data will be used. Confidential company data, personal information and live GPS data will not be published.
