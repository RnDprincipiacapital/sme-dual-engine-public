# Company Universe Collection Plan

- Status: `ready`
- Request rows: 108
- Wave size: 20
- Waves: 6
- Galway rows: 54
- Dublin rows: 54

## Operator Steps

1. Start with wave 1 and keep collection_priority order unless a source owner supplies a full export.
2. Use cro_address_count_url for public company-count baselines where CRO Open Services access is available.
3. Use cro_address_search_url or an approved bulk export to get company-number join keys.
4. Attach the private director-level export and run the director export validator before aggregation.
5. Merge only rows that pass strict director-age import validation and include source approval metadata.

- Private data policy: Do not commit or publish a filled director-level export; publish only aggregate approved company rows.

## Waves

| Wave | Priorities | Rows | County split | Gap split | Top local areas |
| ---: | --- | ---: | --- | --- | --- |
| 1 | 1-20 | 20 | Galway: 20 | missing_row: 20 | Galway / Athenry: 5, Galway / Galway City: 5, Galway / Oranmore: 5, Galway / Salthill: 5 |
| 2 | 21-40 | 20 | Galway: 20 | missing_row: 20 | Galway / Ballinasloe: 6, Galway / Loughrea: 5, Galway / Tuam: 5, Galway / Gort: 3, Galway / Athenry: 1 |
| 3 | 41-60 | 20 | Dublin: 12, Galway: 8 | missing_row: 20 | Galway / Clifden / Connemara: 6, Dublin / Dublin 2 / Docklands: 5, Dublin / Dublin City Centre: 5, Dublin / Dublin 4 / Ballsbridge: 2, Galway / Gort: 2 |
| 4 | 61-80 | 20 | Dublin: 20 | missing_row: 20 | Dublin / Dublin 6 / Rathmines: 5, Dublin / Dublin 8 / Liberties: 5, Dublin / Swords / North County: 5, Dublin / Dublin 4 / Ballsbridge: 3, Dublin / Blanchardstown / West Dublin: 2 |
| 5 | 81-100 | 20 | Dublin: 14, Galway: 6 | incomplete_row: 7, missing_row: 13 | Dublin / Dun Laoghaire / South County: 5, Dublin / Tallaght / South West: 5, Dublin / Blanchardstown / West Dublin: 3, Dublin / Dublin City Centre: 1, Galway / Galway City: 1 |
| 6 | 101-108 | 8 | Dublin: 8 | incomplete_row: 8 | Dublin / Blanchardstown / West Dublin: 1, Dublin / Dublin 2 / Docklands: 1, Dublin / Dublin 4 / Ballsbridge: 1, Dublin / Dublin 6 / Rathmines: 1, Dublin / Dublin 8 / Liberties: 1 |

## Active Wave Rows

| Priority | Batch ID | County | Local area | Sector | Gap | CRO count | CRO search |
| ---: | --- | --- | --- | --- | --- | --- | --- |
| 1 | `galway-company-001` | Galway | Galway City | Consumer Discretionary | `missing_row` | [count](https://services.cro.ie/cws/companycount?company_bus_ind=C&address=Galway+City&format=json) | [search](https://services.cro.ie/cws/companies?company_bus_ind=C&address=Galway+City&format=json&skip=0&max=250&sortBy=company_name&sortDir=asc) |
| 2 | `galway-company-002` | Galway | Galway City | Consumer Staples | `missing_row` | [count](https://services.cro.ie/cws/companycount?company_bus_ind=C&address=Galway+City&format=json) | [search](https://services.cro.ie/cws/companies?company_bus_ind=C&address=Galway+City&format=json&skip=0&max=250&sortBy=company_name&sortDir=asc) |
| 3 | `galway-company-003` | Galway | Galway City | Health Care | `missing_row` | [count](https://services.cro.ie/cws/companycount?company_bus_ind=C&address=Galway+City&format=json) | [search](https://services.cro.ie/cws/companies?company_bus_ind=C&address=Galway+City&format=json&skip=0&max=250&sortBy=company_name&sortDir=asc) |
| 4 | `galway-company-004` | Galway | Galway City | Information Technology | `missing_row` | [count](https://services.cro.ie/cws/companycount?company_bus_ind=C&address=Galway+City&format=json) | [search](https://services.cro.ie/cws/companies?company_bus_ind=C&address=Galway+City&format=json&skip=0&max=250&sortBy=company_name&sortDir=asc) |
| 5 | `galway-company-005` | Galway | Galway City | Financials | `missing_row` | [count](https://services.cro.ie/cws/companycount?company_bus_ind=C&address=Galway+City&format=json) | [search](https://services.cro.ie/cws/companies?company_bus_ind=C&address=Galway+City&format=json&skip=0&max=250&sortBy=company_name&sortDir=asc) |
| 6 | `galway-company-006` | Galway | Salthill | Consumer Discretionary | `missing_row` | [count](https://services.cro.ie/cws/companycount?company_bus_ind=C&address=Salthill%2C+Galway&format=json) | [search](https://services.cro.ie/cws/companies?company_bus_ind=C&address=Salthill%2C+Galway&format=json&skip=0&max=250&sortBy=company_name&sortDir=asc) |
| 7 | `galway-company-007` | Galway | Salthill | Consumer Staples | `missing_row` | [count](https://services.cro.ie/cws/companycount?company_bus_ind=C&address=Salthill%2C+Galway&format=json) | [search](https://services.cro.ie/cws/companies?company_bus_ind=C&address=Salthill%2C+Galway&format=json&skip=0&max=250&sortBy=company_name&sortDir=asc) |
| 8 | `galway-company-008` | Galway | Salthill | Health Care | `missing_row` | [count](https://services.cro.ie/cws/companycount?company_bus_ind=C&address=Salthill%2C+Galway&format=json) | [search](https://services.cro.ie/cws/companies?company_bus_ind=C&address=Salthill%2C+Galway&format=json&skip=0&max=250&sortBy=company_name&sortDir=asc) |
| 9 | `galway-company-009` | Galway | Salthill | Information Technology | `missing_row` | [count](https://services.cro.ie/cws/companycount?company_bus_ind=C&address=Salthill%2C+Galway&format=json) | [search](https://services.cro.ie/cws/companies?company_bus_ind=C&address=Salthill%2C+Galway&format=json&skip=0&max=250&sortBy=company_name&sortDir=asc) |
| 10 | `galway-company-010` | Galway | Salthill | Financials | `missing_row` | [count](https://services.cro.ie/cws/companycount?company_bus_ind=C&address=Salthill%2C+Galway&format=json) | [search](https://services.cro.ie/cws/companies?company_bus_ind=C&address=Salthill%2C+Galway&format=json&skip=0&max=250&sortBy=company_name&sortDir=asc) |
| 11 | `galway-company-011` | Galway | Oranmore | Consumer Discretionary | `missing_row` | [count](https://services.cro.ie/cws/companycount?company_bus_ind=C&address=Oranmore%2C+Galway&format=json) | [search](https://services.cro.ie/cws/companies?company_bus_ind=C&address=Oranmore%2C+Galway&format=json&skip=0&max=250&sortBy=company_name&sortDir=asc) |
| 12 | `galway-company-012` | Galway | Oranmore | Consumer Staples | `missing_row` | [count](https://services.cro.ie/cws/companycount?company_bus_ind=C&address=Oranmore%2C+Galway&format=json) | [search](https://services.cro.ie/cws/companies?company_bus_ind=C&address=Oranmore%2C+Galway&format=json&skip=0&max=250&sortBy=company_name&sortDir=asc) |
| 13 | `galway-company-013` | Galway | Oranmore | Health Care | `missing_row` | [count](https://services.cro.ie/cws/companycount?company_bus_ind=C&address=Oranmore%2C+Galway&format=json) | [search](https://services.cro.ie/cws/companies?company_bus_ind=C&address=Oranmore%2C+Galway&format=json&skip=0&max=250&sortBy=company_name&sortDir=asc) |
| 14 | `galway-company-014` | Galway | Oranmore | Information Technology | `missing_row` | [count](https://services.cro.ie/cws/companycount?company_bus_ind=C&address=Oranmore%2C+Galway&format=json) | [search](https://services.cro.ie/cws/companies?company_bus_ind=C&address=Oranmore%2C+Galway&format=json&skip=0&max=250&sortBy=company_name&sortDir=asc) |
| 15 | `galway-company-015` | Galway | Oranmore | Financials | `missing_row` | [count](https://services.cro.ie/cws/companycount?company_bus_ind=C&address=Oranmore%2C+Galway&format=json) | [search](https://services.cro.ie/cws/companies?company_bus_ind=C&address=Oranmore%2C+Galway&format=json&skip=0&max=250&sortBy=company_name&sortDir=asc) |
| 16 | `galway-company-016` | Galway | Athenry | Industrials | `missing_row` | [count](https://services.cro.ie/cws/companycount?company_bus_ind=C&address=Athenry%2C+Galway&format=json) | [search](https://services.cro.ie/cws/companies?company_bus_ind=C&address=Athenry%2C+Galway&format=json&skip=0&max=250&sortBy=company_name&sortDir=asc) |
| 17 | `galway-company-017` | Galway | Athenry | Consumer Discretionary | `missing_row` | [count](https://services.cro.ie/cws/companycount?company_bus_ind=C&address=Athenry%2C+Galway&format=json) | [search](https://services.cro.ie/cws/companies?company_bus_ind=C&address=Athenry%2C+Galway&format=json&skip=0&max=250&sortBy=company_name&sortDir=asc) |
| 18 | `galway-company-018` | Galway | Athenry | Consumer Staples | `missing_row` | [count](https://services.cro.ie/cws/companycount?company_bus_ind=C&address=Athenry%2C+Galway&format=json) | [search](https://services.cro.ie/cws/companies?company_bus_ind=C&address=Athenry%2C+Galway&format=json&skip=0&max=250&sortBy=company_name&sortDir=asc) |
| 19 | `galway-company-019` | Galway | Athenry | Health Care | `missing_row` | [count](https://services.cro.ie/cws/companycount?company_bus_ind=C&address=Athenry%2C+Galway&format=json) | [search](https://services.cro.ie/cws/companies?company_bus_ind=C&address=Athenry%2C+Galway&format=json&skip=0&max=250&sortBy=company_name&sortDir=asc) |
| 20 | `galway-company-020` | Galway | Athenry | Information Technology | `missing_row` | [count](https://services.cro.ie/cws/companycount?company_bus_ind=C&address=Athenry%2C+Galway&format=json) | [search](https://services.cro.ie/cws/companies?company_bus_ind=C&address=Athenry%2C+Galway&format=json&skip=0&max=250&sortBy=company_name&sortDir=asc) |
