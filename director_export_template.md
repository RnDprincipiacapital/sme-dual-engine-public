# Director Export Input Template

Use this header-only CSV shape for the approved CRO/CORE/director-level export before running the aggregation command.

## Required Fields

- `company_number`
- `director_age`
- `appointment_status`
- `county`
- `local_area`
- `gics_sector`
- `source_url`
- `source_date`

## Optional Fields

- `company_name`
- `director_name`
- `resignation_date`
- `gics_industry_group`
- `registered_address`
- `business_activity`

## Accepted Aliases

- `company_number`: `company_number`, `cro_number`, `company_num`, `company_no`
- `director_age`: `director_age`, `age`, `oldest_director_age`
- `appointment_status`: `appointment_status`, `director_status`, `status`
- `resignation_date`: `resignation_date`, `resigned_on`, `director_resignation_date`
- `registered_address`: `registered_address`, `registeredAddress`, `address`, `company_address`
- `local_area`: `local_area`, `town`
- `business_activity`: `business_activity`, `activity`, `nace_description`, `industry`, `category`, `company_name`

## Handling Rules

- Use one row per director appointment.
- Leave resignation_date blank for current directors; populated resignation dates are treated as inactive and skipped.
- The aggregator uses the maximum active director age per company before calculating 50+/55+/60+/65+/70+ thresholds.
- Rows outside Galway/Dublin or outside supported local areas are skipped.
- This template is public-safe because it contains headers only; do not publish a filled director export.

## Aggregation Command

Run the preflight validator first. It catches missing join keys, unsupported geography, bad ages, and rows that will be skipped before aggregation.

```bash
python3 scripts/validate_director_export.py \
  --director-export path/to/approved-director-export.csv \
  --strict
```

```bash
python3 scripts/build_director_age_import_from_export.py \
  --director-export path/to/approved-director-export.csv \
  --company-request company_universe_request/company-universe-export-request.csv \
  --source-note "Approved director export joined by company number." \
  --source-url https://cro.ie/services-and-help/access-to-cro-data/ \
  --source-date YYYY-MM-DD \
  --approved-by "Name" \
  --director-export-source-id cro-bulk-YYYY-MM-DD \
  --strict
```
