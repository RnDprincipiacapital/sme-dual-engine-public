# Galway/Dublin Pilot Evidence Report

## Run Summary

- Input: `samples/galway-sme-dashboard-expanded-public.json`
- Market data: `docs/approved-data/cso-allocated-market-data-2022.csv`
- Company universe data: `docs/evidence/cro-company-count-evidence-2026-06-04/cro-company-count-evidence.csv`
- Target rows loaded: 213
- Deduplicated entities: 197
- Ranked assessments: 197
- Review queue rows: 197

## Data Readiness

- Status: `sample_or_incomplete`
- Score: 84
- Required counties: Dublin, Galway
- Sector-spend counties: Dublin, Galway
- Company-universe counties: Dublin, Galway
- Sector-spend rows: 12
- Company-universe rows: 15
- Universe company count: 469

## Issues

- Approved source collection is 27 of 120 rows.

## Warnings

- some company universe rows are missing director-age threshold counts

## Sector-Spend Sources

- CSO allocated market estimate: 2022 national turnover from AIA30/ANA13/BAA14 allocated to Galway/Dublin by 2023 BRA34 active-enterprise share and mapped to SME Dual Engine starter sectors. | https://data.cso.ie/table/AIA30; https://data.cso.ie/table/ANA13; https://data.cso.ie/table/BAA14; https://data.cso.ie/table/BRA34 | 2022 turnover; 2023 allocation | approved by Benjamin | 12 row(s)

## Company-Universe Sources

- CRO Company Records open-data daily snapshot; company counts only, no director-age bands. | https://opendata.cro.ie/dataset/companies | 2026-06-04 | approved by Benjamin Falkenburg | 15 row(s)

## Next Actions

- Approved source collection is 27 of 120 rows.
- some company universe rows are missing director-age threshold counts
- replace sample/placeholder Galway and Dublin rows with approved source data
