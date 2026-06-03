# Galway/Dublin Collection Batch

- Status: `ready`
- County: `Dublin`
- Kind: `market`
- Market rows: 6
- Company-universe rows: 0
- Total rows: 6

## How To Use

- Fill the generated CSV rows with approved source values.
- Keep the county, local_area, region_label, and gics_sector keys unchanged.
- Add source_note, source_url, source_date, and approved_by for every row.
- Merge the completed CSVs with `scripts/merge_galway_dublin_approved_data.py --strict-preflight`.
