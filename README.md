# SME Dual Engine Public Dashboard

This repository hosts the public, static GitHub Pages version of the SME Dual Engine.

Live site:

[https://rndprincipiacapital.github.io/sme-dual-engine-public/](https://rndprincipiacapital.github.io/sme-dual-engine-public/)

Source engine repo:

[https://github.com/RnDprincipiacapital/SME-Dual_Engine](https://github.com/RnDprincipiacapital/SME-Dual_Engine)

## What This Site Is

This is a sanitized public demo of the SME Dual Engine. It lets a reviewer interact with the current Dual Engine dashboard, inspect public-safe target rankings, view evidence-gate status, read the guide page, and download public artifacts.

The boss-facing workflow is Microsoft-friendly by default: download the formatted Excel pack, open the Boss Pack HTML pages in a browser, or print any Boss Pack page to PDF. CSV files remain available as compatibility fallbacks. JSON remains published for technical review and automation, but it is no longer the primary reviewer path.

It is designed for demonstration and review. The private internal tool remains the source of truth for confidential research, analyst notes, outreach workflow, and non-public company evidence.

## What Is Published

The public site includes:

- `index.html`: interactive Dual Engine dashboard.
- `guide.html`: plain-English guide to the dashboard.
- `boss_pack/index.html`: Microsoft-friendly reviewer landing page.
- `boss_pack/sme_dual_engine_boss_pack.xlsx`: full formatted Excel workbook with all boss-facing tabs.
- `boss_pack/executive_summary.html`: readable executive summary.
- `boss_pack/priority_research.html`: browser table for the priority research queue.
- `boss_pack/priority_research_queue.xlsx`: formatted Excel priority research workbook.
- `boss_pack/target_table.xlsx`: formatted Excel full public target workbook.
- `boss_pack/weekly_review.xlsx`: formatted Excel weekly review workbook.
- `boss_pack/readiness_scorecard.xlsx`: formatted Excel readiness workbook.
- `boss_pack/data_room_checklist.xlsx`: formatted Excel data-room workbook.
- `boss_pack/company_count_evidence.xlsx`: formatted Excel company-evidence workbook.
- `boss_pack/priority_research_queue.csv`: CSV fallback for the priority research queue.
- `boss_pack/target_table.csv`: CSV fallback for the full public target table.
- `boss_pack/weekly_review.html`: readable weekly review page.
- `boss_pack/readiness_scorecard.html`: readable readiness scorecard.
- `boss_pack/data_room_checklist.html`: readable data-room checklist.
- `targets.json`: technical public-safe target universe.
- `rankings.json`: technical ranked public-safe target output.
- `priority_research_queue.json`: technical priority research queue.
- `evidence_gate_summary.json`: evidence gate summary.
- `collection_progress.json`: approved public-source coverage.
- `cro_company_evidence/cro-company-count-evidence.json`: combined company-count evidence.

The current public build uses public-safe data only and separates boss-friendly outputs from technical audit files.

## Data Safety

Do not commit any of the following to this public hosting repo:

- private backend exports;
- confidential company lists;
- analyst-only notes;
- credentials or tokens;
- private contact workflow history;
- non-public source files;
- client data.

This repo should only contain generated public artifacts that are safe to share.

## How It Is Updated

The site is generated from the source engine repo:

```bash
cd SME-Dual_Engine
python3 scripts/publish_public_dashboard.py --push
```

After publishing, verify the live site:

```bash
python3 - <<'PY'
from dual_engine.public_dashboard_verification import verify_live_dashboard
import json
print(json.dumps(
    verify_live_dashboard(
        live_url="https://rndprincipiacapital.github.io/sme-dual-engine-public/",
        expected_approved_rows=33,
    ),
    indent=2,
))
PY
```

## Current Build Notes

The public dashboard currently includes:

- Dual Engine Playground;
- evidence gate status;
- priority research queue;
- SME sector/subsector taxonomy;
- company-count evidence;
- sale-listing feed section;
- guide page;
- Boss Pack HTML pages;
- formatted Excel workbook downloads;
- Excel-compatible CSV fallbacks;
- technical JSON artifacts for audit and automation.

Company-count evidence combines approved CRO rows with observed public-profile operating SME rows. Observed public-profile evidence is lower-bound evidence, not a full company census.

## Public URL

[https://rndprincipiacapital.github.io/sme-dual-engine-public/](https://rndprincipiacapital.github.io/sme-dual-engine-public/)
