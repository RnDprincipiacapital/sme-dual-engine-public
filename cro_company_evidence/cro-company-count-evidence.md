# CRO Company Count Evidence

- Status: `ready`
- Source: [CRO Company Records](https://opendata.cro.ie/dataset/companies)
- Source date: 2026-06-24
- Output rows: 15
- Total company count: 471

## Approval Blockers

- Director-age threshold counts are not present in CRO Company Records.
- Rows cannot be promoted to approved company-universe inputs until director_50_plus through director_70_plus counts are supplied by an approved director-level source.

## Use

- Use this artifact to validate company-count coverage by county, local area, and GICS sector.
- Join a director-level approved export by CRO company number before filling director-age threshold counts.
- Do not merge this file as an approved company-universe CSV while approval_status is `company_count_only_needs_director_age_source`.
