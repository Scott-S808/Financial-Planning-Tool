# Festival Financial Planner
**MBA 6223 Finance — Spring 2026 | Fisher College of Business | Professor Itzhak Ben-David**

---

## Project Overview

An interactive web tool that calculates the true all-in cost of attending a music festival and frames it using core finance concepts: Time Value of Money, Opportunity Cost, Scenario Analysis, and Risk-Return Tradeoff.

**Live demo:** https://[team-username].github.io/festival-financial-planner

---

## Team

| Role | Name |
|------|------|
| Tech Lead | [Name] |
| Finance Lead | [Name] |
| Design / UX Lead | [Name] |
| Research / Content Lead | [Name] |

---

## Repo Structure

```
/
├── index.html        # The full working tool (single file, no dependencies)
├── CLAUDE.md         # This file — project conventions for Claude Code
├── writeup/
│   └── festival_writeup.docx
└── slides/
    └── festival_slides.pptx
```

---

## Conventions for Claude Code

- **Single file architecture** — all HTML, CSS, and JS lives in `index.html`. Do not split into separate files unless explicitly discussed.
- **No external dependencies** — the tool must run in any browser without an internet connection or install step. Do not add npm packages, CDN imports, or frameworks.
- **Finance formulas are locked** — do not modify the core calculation logic (TVM savings timeline, FV opportunity cost, tier multipliers) without Finance Lead approval.
- **Preserve the three spending tiers** — Budget / Mid / Baller multipliers are defined near the top of the script block. Changes here affect all cost categories simultaneously.
- **Variable naming** — cost variables use snake_case (e.g. `flight_cost`, `lodging_total`). Keep consistent.
- **Comments** — add a short comment above any formula block explaining the finance concept it implements.

---

## Finance Concepts Implemented

| Concept | Course Week | Where in Code |
|---------|-------------|---------------|
| Time Value of Money | Week 1 | `weeksNeeded = perPerson / weeklySavings` |
| Opportunity Cost | Week 2 | `FV = perPerson * Math.pow(1.08, t)` |
| Scenario Analysis | Week 2 | `flightCosts`, `lodgingCosts`, `foodPerDay` tier objects |
| Risk-Return Tradeoff | Week 8 | Verdict logic (`weeksNeeded` thresholds) |

---

## Running Locally

No setup required. Just open `index.html` in any browser.

```bash
open index.html        # Mac
start index.html       # Windows
xdg-open index.html    # Linux
```

---

## Deploying to GitHub Pages

1. Push changes to the `main` branch
2. Go to **Settings → Pages**
3. Set source to **Deploy from branch → main → / (root)**
4. Live URL will be: `https://[team-username].github.io/festival-financial-planner`

---

## Submission Checklist

- [ ] `index.html` — working tool, tested in Chrome and Safari
- [ ] `CLAUDE.md` — this file, team names filled in
- [ ] `writeup/festival_writeup.docx` — 2-page writeup, team names filled in
- [ ] `slides/festival_slides.pptx` — presentation deck, team names filled in
- [ ] GitHub Pages URL is live and shareable
- [ ] All team members have pushed at least one commit
