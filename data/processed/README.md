# Processed Data

This folder will contain cleaned or transformed datasets created during the project.

## Planned processing steps

1. Profile the raw data
2. Standardize column names
3. Convert dates and timestamps
4. Standardize units
5. Handle missing values
6. Remove or investigate duplicates
7. Validate relationships between tables
8. Create analysis-ready datasets

## Data-quality rules

Every processed dataset should be checked for:

- Correct row counts
- Duplicate records
- Missing identifiers
- Invalid dates
- Invalid numeric values
- Unexpected categories
- Broken relationships between tables

The cleaning logic should be documented in the SQL scripts or Python notebooks that create each dataset.
