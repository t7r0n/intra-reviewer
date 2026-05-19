# Intra Reviewer

A rubric aware, project specific code & artifact reviewer that gives Turing College students Sprint 1 grade feedback within 4 minutes of pushing - and routes the genuinely stuck cases to human mentors with the right context attached.

## Why This Exists

Turing College sells project based learning with 1:1 mentor reviews (AI Engineering page). But mentor capacity is the hard ceiling on the model - they have "150+ industry mentors" and a goal of "1 on 1 tutoring accessible 24/7" (Lukas interview).

## What It Builds

- Replays synthetic `turing` and `college` cases against the project's evidence rules.
- Scores `turing_coverage`, `college_risk`, and `sells_precision` so regressions are visible in CSV and JSON.
- Plants `turing drift` and `college gap` failures as negative controls.
- Writes citation-locked decision claims; unsupported claims fail verification.
- Exports a review dashboard and demo pack for `intra-reviewer` without hosted services.

## Local Run

```bash
uv sync
uv run intra-reviewer all
uv run pytest -q
uv run ruff check .
```

## Outputs

- `outputs/analysis.json`
- `outputs/scenario_report.csv`
- `outputs/decision_report.md`
- `outputs/evidence_packet.md`
- `outputs/dashboard.html`
- `outputs/demo_pack.zip`

## Sources

- https://en.wikipedia.org/wiki/Turing_College_(edtech_company
- https://www.turingcollege.com/ai-engineering
- https://www.turingcollege.com/software-and-ai-engineering
- https://www.turingcollege.com/blog/lukas-kaminskis-interview
- https://www.turingcollege.com/blog/data-science-analytics-masters-degree
- https://www.coursereport.com/schools/turing-college
- https://www.crunchbase.com/organization/turing-college
- https://moge.ai/product/turing-college
- https://www.turingcollege.com/blog/ai-engineer-roadmap-how-to-become-an-ai-engineer

## Boundary

This repository uses synthetic fixtures only. It has no credentials, no customer data, no outreach data, and no dependency on a hosted API.
