# Director-Age Source Plan

- Status: `director_age_source_required`
- Approved rows: 27 / 120
- Remaining row gaps: 108
- Company-universe request rows: 108
- Company-count-only rows waiting on director ages: 15
- CRO company-count evidence total: 471

## Why This Is Still Missing

The public site can show observed market breadth today, but the approved company-universe gate remains open until director-age threshold counts are supplied by an approved director-level source.

## Required Fields

- `company_number`
- `county`
- `local_area`
- `sme_sector_or_gics_sector`
- `company_count`
- `director_50_plus_count`
- `director_55_plus_count`
- `director_60_plus_count`
- `director_65_plus_count`
- `director_70_plus_count`
- `source_note`
- `source_url`
- `source_date`
- `approved_by`

## Source Routes

### CRO bulk-data customer extract

- Status: `needs_access`
- Access model: `licensed_bulk_data`
- Source: [Companies Registration Office](https://cro.ie/services-and-help/access-to-cro-data/)
- Expected fields: company_number, director_name, director_address, appointment_date, resignation_date
- Use: Join director appointments to CRO company numbers, derive active-director age thresholds if date-of-birth or age metadata is included in the approved extract.
- Note: CRO states that bulk data is supplied to customers through a secure location using individual login credentials.

### CORE account-holder company printout / appointment download

- Status: `manual_or_paid`
- Access model: `account_holder_or_document_purchase`
- Source: [Companies Registration Office](https://cro.ie/services-and-help/using-services/)
- Expected fields: company_number, director_names, secretary_names, submissions, appointment_documents
- Use: Validate director/officer identities for priority companies when bulk export is unavailable.
- Note: CORE search supports viewing company data by name or number; document and appointment detail may require account workflows.

### CRO Open Data Company Records

- Status: `connected_for_company_counts_only`
- Access model: `open_data`
- Source: [Companies Registration Office](https://opendata.cro.ie/dataset/companies)
- Expected fields: company_number, company_name, company_status, registered_office, nace_code
- Use: Keep company counts, status, geography, and sector evidence current.
- Note: This route does not supply the director-age threshold fields required for approved company-universe rows.

## Next Actions

1. Obtain a director-level CRO/CORE/bulk export keyed by company number for the 108 request rows.
2. Join the director-level export to the existing CRO company-count evidence by company number and active appointment status.
3. Aggregate active companies by county, local area, and sector into director_50_plus through director_70_plus threshold counts.
4. Merge only rows with complete threshold counts and approval metadata into the approved company-universe CSV.
