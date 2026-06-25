# Company Universe Work Queue

- Status: `open`
- Open work items: 108
- Wave count: 6
- Active wave: 1
- Private data policy: Do not commit or publish a filled director-level export; publish only aggregate approved company rows.

## Operator Steps

1. Start with wave 1 and keep collection_priority order unless a source owner supplies a full export.
2. Use cro_address_count_url for public company-count baselines where CRO Open Services access is available.
3. Use cro_address_search_url or an approved bulk export to get company-number join keys.
4. Attach the private director-level export and run the director export validator before aggregation.
5. Merge only rows that pass strict director-age import validation and include source approval metadata.

## Wave Summary

| Wave | Open rows |
| ---: | ---: |
| 1 | 20 |
| 2 | 20 |
| 3 | 20 |
| 4 | 20 |
| 5 | 20 |
| 6 | 8 |

## Active Wave Queue

| Priority | Work item | County | Local area | Sector | Missing fields | Company count | Director age |
| ---: | --- | --- | --- | --- | ---: | --- | --- |
| 1 | `wave-01-galway-company-001` | Galway | Galway City | Consumer Discretionary | 11 | missing | missing |
| 2 | `wave-01-galway-company-002` | Galway | Galway City | Consumer Staples | 11 | missing | missing |
| 3 | `wave-01-galway-company-003` | Galway | Galway City | Health Care | 11 | missing | missing |
| 4 | `wave-01-galway-company-004` | Galway | Galway City | Information Technology | 11 | missing | missing |
| 5 | `wave-01-galway-company-005` | Galway | Galway City | Financials | 11 | missing | missing |
| 6 | `wave-01-galway-company-006` | Galway | Salthill | Consumer Discretionary | 11 | missing | missing |
| 7 | `wave-01-galway-company-007` | Galway | Salthill | Consumer Staples | 11 | missing | missing |
| 8 | `wave-01-galway-company-008` | Galway | Salthill | Health Care | 11 | missing | missing |
| 9 | `wave-01-galway-company-009` | Galway | Salthill | Information Technology | 11 | missing | missing |
| 10 | `wave-01-galway-company-010` | Galway | Salthill | Financials | 11 | missing | missing |
| 11 | `wave-01-galway-company-011` | Galway | Oranmore | Consumer Discretionary | 11 | missing | missing |
| 12 | `wave-01-galway-company-012` | Galway | Oranmore | Consumer Staples | 11 | missing | missing |
| 13 | `wave-01-galway-company-013` | Galway | Oranmore | Health Care | 11 | missing | missing |
| 14 | `wave-01-galway-company-014` | Galway | Oranmore | Information Technology | 11 | missing | missing |
| 15 | `wave-01-galway-company-015` | Galway | Oranmore | Financials | 11 | missing | missing |
| 16 | `wave-01-galway-company-016` | Galway | Athenry | Industrials | 11 | missing | missing |
| 17 | `wave-01-galway-company-017` | Galway | Athenry | Consumer Discretionary | 11 | missing | missing |
| 18 | `wave-01-galway-company-018` | Galway | Athenry | Consumer Staples | 11 | missing | missing |
| 19 | `wave-01-galway-company-019` | Galway | Athenry | Health Care | 11 | missing | missing |
| 20 | `wave-01-galway-company-020` | Galway | Athenry | Information Technology | 11 | missing | missing |

## Acceptance Gate

- A row is not ready for merge until company_count, all five director-age thresholds, source_note, source_url, source_date, and approved_by are populated.
- The strict validators pass: director export and director-age import validators must pass before the public dashboard treats rows as approved.
- Do not publish a filled director-level export; publish only aggregate approved company-universe rows.
