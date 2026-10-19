# Engineering task scope — Systems Builder (AI · Software · Systems)

Status: role lens · Task list: [`jj.md`](jj.md) · Source: `../TASKS.md` (99 tasks) · 16.OCT.2026

This is the engineering slice of the task backlog: what the AI Engineer / Software
Engineer / Systems Builder owns, in what order, and with what interfaces. The numbered
task list itself — 11 main tasks with 41 subtasks, carrying time, donation impact, and priority — lives in
[`jj.md`](jj.md); this document is the role lens on it. T-xx references belong to the
organisation-wide backlog in `TASKS.md`.

## 1. Mandate

Own the data layer, the automations, and the Slack AI agent (Leleka). Build the systems the other pillars
run on: integrations, pipelines, reconciliation, fulfillment automation.

- **Build once, reuse:** the dashboard data layer (JJ-03) is also Leleka's data layer — never two integration stacks.
- **Protect the money routes first:** nothing that touches existing donor payments gets replaced without running old and new in parallel first.
- **Exceptions are visible:** every automation keeps a manual path for unmatched/rejected cases.
- **Sensitive data:** donor records in scope — self-hosted tooling preferred (see §6).

Scope size: **38 Eng-owned + 3 shared tasks**. Distribution: P0 = 18 Eng,
P1 = 16 Eng, P2 = 1 Eng, P3 = 3 Eng.

## 2. Owner map (TASKS.md column "Owner")

| Code | Who | Examples |
| --- | --- | --- |
| **Eng** | This role | Dashboard, payment matching, Leleka, BTCPay, packing exports |
| **Ops** | Functional operations (MilOps / DonorOps / OrgOps runs, leads, records) | Approval, convoy planning, packing dispatch, access audit |
| **Mkt** | Marketing & fundraising | Campaigns, promotion, market expansion, JP partner |
| **Web** | Website developer (contract) | Campaign pages, translations, site work |
| **Shared** | Joint ownership (Eng + named pillar) | Flow streamlining, emergency lockout |

## 3. Build tracks

| # | Track | Tasks | Est. | Why it matters |
| --- | --- | --- | --- | --- |
| 1 | Discovery | JJ-01.1, JJ-01.2, JJ-02.1, JJ-02.2 | 1–2 wk | Cheapest risk reduction; unlocks everything after |
| 2 | Data layer → dashboard | JJ-03.1–JJ-03.4 | 5–8 wk | The manual's immediate deliverable; doubles as Leleka's layer |
| 3 | Donation protection + fulfillment | JJ-04.1–JJ-04.3, JJ-05.1–JJ-05.6 | 8–12 wk | Protects ~€70k/mo recurring and automates the primary workflow |
| 4 | Video pipeline | JJ-06.1 → JJ-06.2 → JJ-06.3 | 4–6 wk | Donor experience (primary automation target) |
| 5 | Shipping automation | JJ-07.1 → JJ-07.2 → JJ-07.3 | 4–6 wk | Fulfillment economics; pick 4 or 5 first |
| 6 | Leleka (Slack agent) | JJ-01.3, JJ-01.4, JJ-01.5 | 6–10 wk | Insights agent; gated on track 2's data layer |
| 7 | Growth builds | JJ-08.1, JJ-08.2, JJ-08.3 | parallel | New crypto payment channels (not a priority for now) |
| 8 | MilOps + ops tooling | JJ-09.1–JJ-09.4, JJ-10.1–JJ-10.3 | parallel | Utility builds and risk tooling |
| 9 | Social publishing | JJ-11.1 → JJ-11.3 → JJ-11.2 → JJ-11.5 (JJ-11.4 optional) | parallel | Campaign reach without manual posting; per-channel donation attribution |

## 4. First 90 days

1. **Weeks 1–2 — decisions, not code.** JJ-01.1/JJ-01.2 (Leleka: use cases, platform choice),
   JJ-02.1/JJ-02.2 (payment/goods flow map, TypeForm integrate-vs-eliminate). Outputs: short memos
   the team can act on.
2. **Weeks 2–8 — data layer.** JJ-04.1 first (subscription reconciliation across donation accounts — the
   direct revenue-protection win), then the dashboard (JJ-03.1–JJ-03.4). The weekly core-team review (T-10) starts
   running on it with Ops.
3. **Weeks 8–13 — automation.** JJ-04.2 → JJ-05.1/JJ-05.2 (matching → intake → eligibility), then
   commit to one experience track: video (JJ-06) or shipping (JJ-07).

## 5. Task list (Eng-owned + shared)

See [`jj.md`](jj.md) — 11 main tasks with 41 subtasks, each with time, donation impact, and priority.

## 6. Interfaces & constraints (manual §5.4)

- Preserve the legacy subscription channel and all existing payment routes; no forced migration (T-20 guardrail).
- Keep unit-intake forms and donor-fulfillment forms distinct.
- Work through the website developer and the donation-platform account manager; specialist platform support via T-69.
- Sensitive-data review before any Leleka/donor-data work (JJ-01.3) — self-hosted agent preferred (platform evaluation, JJ-01.2).
- Reporting discipline: totals must trace to source reports; missing feeds flagged, refresh times visible (JJ-03.1 requirements).
- Crypto stays separate from US tax-deductible reporting (JJ-03.3 note).

## 7. Day-one access checklist

Provisioned via Ops (T-88 register, T-90 checklist — after T-87 audit cleanup):

- CRM (deals, stages) · donation platform (reporting/admin read where possible)
- Google Workspace / Drive / core spreadsheets · website repo + hosting
- Zapier account · postal system accounts (read/export) · Slack
- Web analytics + social reporting · issue tracker + this repo

## 8. Skills profile

API integrations (CRM, donation platforms, Google Workspace, postal) · data pipelines and
reconciliation · self-hosted LLM agents (chat/insights) · web front-end for forms/checkout ·
light security and access tooling. Comfortable working with non-technical process owners.

## 9. Working agreements

- Every shipped build lands back in `TASKS.md` (and the issue tracker) with owner + status.
- Replacement of anything live (payment flows, the Zapier bot “Sniffer”, TypeForm) happens behind a parallel run (old + new) with a rollback path.
- Automations keep a manual exception path — unmatched payments, unlinked videos, held stock stay visible.
- Related effort: the `demo.help69.si` board project covers overlapping fulfillment/reconciliation work packages — coordinate before building parallel solutions.
