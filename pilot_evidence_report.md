# Galway/Dublin Pilot Evidence Report

## Run Summary

- Input: `samples/galway-sme-dashboard-expanded-public.json`
- Market data: `docs/approved-data/cso-allocated-market-data-2022.csv`
- Company universe data: `docs/evidence/cro-company-count-evidence-2026-06-25/cro-company-count-evidence.csv`
- Target rows loaded: 326
- Deduplicated entities: 310
- Ranked assessments: 310
- Review queue rows: 310

## Data Readiness

- Status: `sample_or_incomplete`
- Score: 84
- Required counties: Dublin, Galway
- Sector-spend counties: Dublin, Galway
- Company-universe counties: Dublin, Galway
- Sector-spend rows: 12
- Company-universe rows: 15
- Universe company count: 472

## Issues

- Approved source collection is 27 of 120 rows.

## Warnings

- No readiness warnings detected.

## Sector-Spend Sources

- CSO allocated market estimate: 2022 national turnover from AIA30/ANA13/BAA14 allocated to Galway/Dublin by 2023 BRA34 active-enterprise share and mapped to SME Dual Engine starter sectors. | https://data.cso.ie/table/AIA30; https://data.cso.ie/table/ANA13; https://data.cso.ie/table/BAA14; https://data.cso.ie/table/BRA34 | 2022 turnover; 2023 allocation | approved by Benjamin | 12 row(s)

## Company-Universe Sources

- CRO Company Records open-data daily snapshot; company-count evidence by local area and sector. | https://opendata.cro.ie/dataset/companies | 2026-06-25 | approved by Benjamin Falkenburg | 15 row(s)

## Next Actions

- Approved source collection is 27 of 120 rows.
- replace sample/placeholder Galway and Dublin rows with approved source data
