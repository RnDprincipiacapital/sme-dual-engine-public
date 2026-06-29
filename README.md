# SME Dual Engine Public Dashboard

This repository hosts the public, static GitHub Pages version of the SME Dual Engine.

Live site:

[https://rndprincipiacapital.github.io/sme-dual-engine-public/](https://rndprincipiacapital.github.io/sme-dual-engine-public/)

Source engine repo:

[https://github.com/RnDprincipiacapital/SME-Dual_Engine](https://github.com/RnDprincipiacapital/SME-Dual_Engine)

## What This Site Is

This is a sanitized public demo of the SME Dual Engine. It lets a reviewer interact with the current Dual Engine dashboard, inspect public-safe target rankings, view evidence-gate status, read the guide page, and download public artifacts.

It is designed for demonstration and review. The private internal tool remains the source of truth for confidential research, analyst notes, outreach workflow, and non-public company evidence.

## What Is Published

The public site includes:

- `index.html`: interactive Dual Engine dashboard.
- `guide.html`: plain-English guide to the dashboard.
- `targets.json`: public-safe target universe.
- `rankings.json`: ranked public-safe target output.
- `priority_research_queue.json`: priority research queue.
- `weekly_review_report.md`: weekly review output.
- `evidence_gate_summary.json`: evidence gate summary.
- `collection_progress.json`: approved public-source coverage.
- `cro_company_evidence/cro-company-count-evidence.json`: combined company-count evidence.
- `investment_readiness_scorecard.md`: readiness scorecard.
- `data_room_checklist.md`: public-safe data-room checklist.

The current public build uses public-safe data only and shows `33 / 120` approved source rows.

## Data Safety

Do not commit any of the following to this public hosting repo:

- private backend exports;
- confidential company lists;
- analyst private notes;
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
- downloadable public artifacts.

Company-count evidence combines approved CRO rows with observed public-profile operating SME rows. Observed public-profile evidence is lower-bound evidence, not a full company census.

## Public URL

[https://rndprincipiacapital.github.io/sme-dual-engine-public/](https://rndprincipiacapital.github.io/sme-dual-engine-public/)
