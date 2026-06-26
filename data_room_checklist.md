# Investment-Grade Data Room Checklist

- Status: `data_room_required`
- Approved rows: 27 / 120
- Remaining row gaps: 93
- Company-universe request rows: 93
- Collection waves: 5
- Advertised sale listings: 226

## Summary

The dashboard is interactive and public-safe, but 93 source rows still need approved company-count evidence and source metadata before investment-grade use.

## Downloads

- [Company collection plan](company_universe_request/company-universe-collection-plan.md)
- [Company export request](company_universe_request/company-universe-export-request.csv)
- [Company work queue](company_universe_request/company-universe-work-queue.csv)
- [CRO company evidence](cro_company_evidence/cro-company-count-evidence.csv)

## Required Data

### 1. Approved company-count evidence

- Status: `required`
- Owner: Research operator using approved public/company-registry sources
- Required for: 93 company-universe rows that need approved counts or metadata.
- Accepted format: Completed company-universe-wave-N.csv rows with company_count, source_note, source_url, source_date, and approved_by filled.
- Approval gate: Strict company-universe preflight passes with no missing company_count or approval metadata.
- Public/private rule: Publish aggregate company-count evidence only; do not publish private enrichment exports.

### 2. Completed company-universe waves

- Status: `required`
- Owner: Research operator using the published wave CSVs
- Required for: Moving all Galway/Dublin local-area and sector rows from request status to approved status.
- Accepted format: Completed wave CSVs that reconcile to the company export request.
- Approval gate: Each completed wave merges cleanly through the approved-data workflow.
- Public/private rule: Wave CSVs may stay public while they contain request rows and aggregate evidence only.

### 3. CRO/company-source reconciliation

- Status: `required`
- Owner: Company registry data owner or source reviewer
- Required for: Company-count baseline checks before approved rows are merged.
- Accepted format: CRO/company evidence CSV plus source URL, source date, and reviewer approval fields.
- Approval gate: Approved company counts reconcile to the company universe before dashboard promotion.
- Public/private rule: Publish source class, public URL, and aggregate counts only.

### 4. Sale-listing feed review

- Status: `ready`
- Owner: Origination analyst
- Required for: Keeping advertised-for-sale targets fresh and removing duplicates or irrelevant listings.
- Accepted format: Published sale listing audit with URL, source, observed date, and listing metadata.
- Approval gate: Public sale refresh audit returns status ok and stale or duplicate rows are reviewed.
- Public/private rule: Public listing metadata and source URLs are publishable; private broker notes are not.

### 5. Approval metadata

- Status: `required`
- Owner: Investment or data-quality reviewer
- Required for: Moving rows from sample/incomplete to approved in the dashboard readiness gate.
- Accepted format: source_note, source_url, source_date, approved_by, and validation report references.
- Approval gate: Approved source collection reaches 120 of 120 rows with no placeholder or missing approval fields.
- Public/private rule: Approval metadata can be published when it identifies source class and reviewer without private personal data.

## Success Definition

- All 120 expected public-source rows are approved.
- All company-universe rows have approved company_count evidence and source metadata.
- No private enrichment export or personal data is committed or published.
- Live dashboard verifier passes with collection_progress_status approved_collection_complete.
