# Galway/Dublin Collection Pack

- Status: `ready`
- Market rows: 0
- Company-universe rows: 93
- Total rows: 93

## Files

| County | Kind | Rows | CSV | Notes |
| --- | --- | ---: | --- | --- |
| Galway | market | 0 | `galway-market.csv` | `galway-market.md` |
| Galway | company | 48 | `galway-company.csv` | `galway-company.md` |
| Dublin | market | 0 | `dublin-market.csv` | `dublin-market.md` |
| Dublin | company | 45 | `dublin-company.csv` | `dublin-company.md` |

## How To Use

- Start with the county and kind you are actively sourcing.
- Fill every blank value from an approved source.
- Keep county, local_area, region_label, and gics_sector keys unchanged.
- Every completed row needs source_note, source_url, source_date, and approved_by.
- Merge completed rows with `scripts/merge_galway_dublin_approved_data.py --strict-preflight`.
