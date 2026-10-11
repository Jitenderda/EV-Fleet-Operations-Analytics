# Data Dictionary

**Status:** Initial draft  
**Purpose:** Define the planned tables, their grain and important fields before implementation.

## 1. vehicles

**Grain:** One row per vehicle.

| Column | Description |
|---|---|
| vehicle_id | Unique vehicle identifier |
| model | Vehicle model |
| model_year | Manufacturing or model year |
| battery_capacity_kwh | Usable battery capacity |
| depot_id | Assigned depot |
| fleet_status | Active, inactive or under maintenance |

## 2. stations

**Grain:** One row per charging station.

| Column | Description |
|---|---|
| station_id | Unique station identifier |
| station_name | Station name |
| city | Station city |
| depot_id | Related depot |
| charger_type | AC, DC or other type |
| connector_count | Number of available connectors |
| maximum_power_kw | Maximum charging power |

## 3. trips

**Grain:** One row per completed vehicle trip.

| Column | Description |
|---|---|
| trip_id | Unique trip identifier |
| vehicle_id | Vehicle used for the trip |
| start_time | Trip start timestamp |
| end_time | Trip end timestamp |
| distance_km | Trip distance |
| energy_used_kwh | Energy used during the trip |
| start_soc_pct | Battery percentage at trip start |
| end_soc_pct | Battery percentage at trip end |
| route_zone | Anonymized route or operating zone |

## 4. charging_sessions

**Grain:** One row per charging attempt.

| Column | Description |
|---|---|
| session_id | Unique charging-session identifier |
| vehicle_id | Vehicle being charged |
| station_id | Charging station used |
| start_time | Charging start timestamp |
| end_time | Charging end timestamp |
| energy_delivered_kwh | Energy delivered |
| charging_cost | Cost of the session |
| start_soc_pct | Battery percentage before charging |
| end_soc_pct | Battery percentage after charging |
| session_status | Completed, failed or interrupted |

## 5. battery_snapshots

**Grain:** One row per vehicle per measurement period.

| Column | Description |
|---|---|
| vehicle_id | Vehicle identifier |
| snapshot_time | Measurement timestamp |
| soc_pct | State of charge |
| soh_pct | State of health |
| battery_temperature_c | Battery temperature |
| charging_cycles | Total charging cycles |
| fault_code | Battery or vehicle fault code |

## 6. maintenance_events

**Grain:** One row per maintenance event.

| Column | Description |
|---|---|
| maintenance_id | Unique maintenance-event identifier |
| vehicle_id | Vehicle requiring maintenance |
| event_date | Maintenance date |
| issue_type | Type of issue |
| repair_cost | Repair cost |
| downtime_hours | Vehicle downtime |
| event_status | Open, resolved or cancelled |

## Version 1 scope note

Version 1 will use trip summaries rather than raw second-by-second GPS points.

A raw GPS-points table and real-time IoT telemetry may be added later as optional extensions.

## Questions to confirm before implementation

- What exactly counts as a completed trip?
- How should failed charging attempts be handled?
- Which timezone will be used?
- Are energy values measured or simulated?
- How will missing battery-health readings be treated?
- Are route zones anonymized?
