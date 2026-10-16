# Task backlog — derived from OPS manUAl v2 (05.OCT.2026)

Source: `docs/README.md`. Existing tasks trace to a manual section (§); T-70+ are
stakeholder additions (16.OCT.2026). Ratings are working estimates pending team review —
time figures describe implementation effort, or effort per occurrence for steady-state
(Run) tasks.

**Legend**

- **Type** — Build (new tooling/system) · Automate (remove manual handling) · Run (steady-state operation) · Explore (research/decision first).
- **Time** — S (<1 day) · M (1–5 days) · L (1–3 weeks) · XL (>1 month). For Run: effort per cycle (payment, batch, campaign, month…).
- **Donation influence** — High: directly grows or protects income/donor experience · Med: supports it indirectly · Low: internal efficiency only.
- **Priority** — P0 now · P1 next · P2 later · P3 backlog.

## Quick wins (High influence, ≤ M time)

| ID | Task | Type | Time | Donation | P |
| --- | --- | --- | --- | --- | --- |
| T-09 | One-time → recurring conversion email flow | Automate | S–M | High | P0 |
| T-30 | Auto-send donor email after subtitles (dedupe + retry) | Automate | M | High | P1 |
| T-32 | Handover filming per vehicle (donor thank-you asset) | Run | S | High | P1 |
| T-33 | Subtitle + translate donor videos | Run | S–M | High | P1 |
| T-34 | Personal thank-you email per donor | Run | S | High | P1 |
| T-75 | Payment + goods-receipt flow mapping (TypeForm et al.) | Explore | S–M | High | P0 |
| T-76 | TypeForm decision: integrate vs eliminate | Explore | S | High | P0 |
| T-81 | BTCPay Server deployment (hosting, wallets, security) | Build | M | High | P1 |

## Suggested sequence

0. **Stakeholder track (very important — start immediately):** T-70/T-71 (Leleka discovery), T-75/T-76 (flow mapping + TypeForm decision), and T-87 (access audit + revoke). Small, and they unblock big builds or remove standing risk.
1. **Dashboard track (P0):** T-01 → T-04, then run the weekly review (T-10). Leleka (T-73) must reuse this reconciled data layer.
2. **Donor-protection track (P0):** T-08 (protect ~€70k/mo legacy recurring) → T-05 → T-06 → T-07 → T-09 → T-77 (streamlined flow build).
3. **New builds once discovery completes (P1):** Leleka T-72 → T-74 · forms/UX T-78 · eCommerce T-79/T-80 · BTCPay T-81 → T-83 · JP T-84 → T-86.
4. **Existing donor-experience completion (P1):** video pipeline T-28 → T-30 in parallel with shipping T-21 → T-23.
5. **Expansion (P1, long horizon):** T-39/T-40 groundwork → T-41 (German) → T-42.
6. **Follow-on builds (P2):** T-48 → T-50 as capacity allows.

## P0 — Now

| ID | Task | § | Type | Time | Donation | P |
| --- | --- | --- | --- | --- | --- | --- |
| T-01 | Build shared reporting dashboard (one period, currency rules, account vs method fields, reconciliation, refresh times, missing-feed flags) | 7.1 | Build | L | High | P0 |
| T-02 | Donation-account feeds into dashboard (campaign receipts, totals, one-time vs recurring) | 7.1 | Build | M | High | P0 |
| T-03 | Bank + crypto records into reconciliation view | 7.1 | Build | M | Med | P0 |
| T-04 | Web analytics + social feeds into dashboard | 7.1 | Build | M | Med | P0 |
| T-05 | Automated payment → donor/campaign/account matching | 7.2 | Automate | L | High | P0 |
| T-06 | Automated benefit-request intake (reuse saved details, capture selections, generate fulfillment record) | 7.2 | Automate | L | High | P0 |
| T-07 | Eligibility rule engine (patch caps; >€750 unit patch; message ≥€1,500, max 4/vehicle; recurring tiers) | 7.2 | Automate | M–L | High | P0 |
| T-08 | Cross-account subscription reconciliation (protect ~700 donors / ~€70k/mo) | 7.2 | Automate | M | High | P0 |
| T-09 | One-time → recurring conversion email flow | 2.2 | Automate | S–M | High | P0 |
| T-10 | Weekly core-team review from one view; flag exceptions | 5.1/7.1 | Run | S/wk | Med | P0 |
| T-11 | US tax-deductible channel upkeep + performance feeds expansion (ceiling ≈ €100k/mo) | 2.3 | Run | M/mo | High | P0 |
| T-12 | Unit approval + campaign prioritization (lead) | 3.2 | Run | S/unit | Med | P0 |
| T-13 | Campaign brief preparation (DOCX, reuse standard content) | 2.1 | Run | S/campaign | High | P0 |
| T-14 | Campaign configuration (donation link + fulfillment form) | 2.1 | Run | S/campaign | High | P0 |
| T-15 | Campaign publication via website developer (site template) | 2.1 | Run | S/campaign | High | P0 |
| T-16 | Campaign promotion (website, professional networks, social channels) | 2.1 | Run | M/campaign | High | P0 |
| T-17 | Request video + subtitles per approved unit | 3.2 | Run | M/unit | High | P0 |
| T-18 | Vehicle sourcing across procurement markets | 3.3 | Run | L/round | Med | P0 |
| T-19 | Campaign/donor references kept attached to payments | 4.1 | Run | S/payment | Med | P0 |
| T-20 | Guardrail: no forced migration of legacy subscriptions | 4.1 | Run | — | High | P0 |
| T-75 | Map current payment + goods-receipt flow (TypeForm, donation platform, postal) | NEW | Explore | S–M | High | P0 |
| T-76 | TypeForm decision: integrate vs eliminate to receive goods | NEW | Explore | S | High | P0 |
| T-77 | Streamlined donation → benefits → payment → product flow (deps T-06/T-07/T-27) | NEW | Build | L | High | P0 |
| T-70 | Leleka: use-case catalogue + data-source inventory (insights people ask for; what's missing) | NEW | Explore | S–M | Med | P0 |
| T-71 | Leleka: platform evaluation — Hermes Agent vs alternatives (Slack path, Zapier bot limits) | NEW | Explore | M | Med | P0 |
| T-72 | Leleka: data access, permissions, sensitive-data review | NEW | Build | M | Med | P0 |
| T-87 | Access audit: list holders per system, cross-check against current team, revoke departures (incl. Google sheets) | NEW | Run | S–M | Med | P0 |

## P1 — Next

| ID | Task | § | Type | Time | Donation | P |
| --- | --- | --- | --- | --- | --- | --- |
| T-21 | Packing list + postal CSV generation (RoW and US formats) | 7.2/4.3 | Automate | L | Med | P1 |
| T-22 | Stock-readiness gating; hold campaign batches until patches available | 4.3/7.2 | Automate | M | Med | P1 |
| T-23 | Bonus/quantity overlap → shipping review flag | 4.2 | Automate | S–M | Low | P1 |
| T-24 | RoW packing + worldwide labels + postal collector handoff | 4.3 | Run | S–M/batch | Med | P1 |
| T-25 | US bulk: domestic labels, consolidation box, local coordinator posting | 4.3 | Run | S–M/batch | Med | P1 |
| T-26 | Reusable, editable donor shipping profile | 7.2 | Build | L | Med | P1 |
| T-27 | Replace proof screenshots with reliable payment matching | 7.2 | Build | M–L | Med | P1 |
| T-28 | Auto-link handover video → vehicle/message/donor | 4.4/7.2 | Automate | L | High | P1 |
| T-29 | Auto-route uploads to subtitle contributors; hold unlinked files | 4.4/7.2 | Automate | M | High | P1 |
| T-30 | Auto-send donor email post-subtitles (duplicate prevention + retry path) | 4.4/7.2 | Automate | M | High | P1 |
| T-31 | Donor message capture into message sheet | 4.4 | Run | S | Med | P1 |
| T-32 | Handover filming per vehicle | 4.4 | Run | S | High | P1 |
| T-33 | Subtitle + translate donor videos | 4.4 | Run | S–M | High | P1 |
| T-34 | Personal thank-you email per donor (correct video) | 4.4 | Run | S | High | P1 |
| T-35 | Monthly €300+ newsletter + extra-patch selection | 4.5 | Run/Automate | M/mo | Med | P1 |
| T-36 | Campaign completion → selection catalogue update | 4.5/7.2 | Automate | S–M | Med | P1 |
| T-37 | Recognition list sync (website + video channel) for active donors | 4.5 | Automate | M | Med | P1 |
| T-38 | Volunteer/other-channel entitlement tracking | 4.5 | Run | S | Med | P1 |
| T-39 | UK tax-deductible channel setup (operating arrangement + donation route) | 2.3 | Explore | XL | High | P1 |
| T-40 | Germany tax-deductible channel setup | 2.3 | Explore | XL | High | P1 |
| T-41 | German-language programme (DE/AT/CH, ≈15% of target audience) | 2.3 | Build | L–XL | High | P1 |
| T-42 | Website translation workstream | 2.3 | Build | L | Med | P1 |
| T-43 | Issue tracker + process map + shared documentation upkeep | 5.2 | Run | S/wk | Med | P1 |
| T-44 | Bank-transfer + crypto reconciliation by payment reference | 4.1 | Run | S–M/mo | Med | P1 |
| T-45 | Donation-platform / website-developer integration support | 5.4/2.1 | Run | S–M | Med | P1 |
| T-46 | Host systems upkeep (CMS, accounts, forms, postal, CRM, sheets, email/video, analytics) | 5.2 | Run | S/wk | Med | P1 |
| T-47 | US account identity carried in donation + reporting records | 4.1 | Run | S | Med | P1 |
| T-81 | BTCPay Server deployment (hosting, wallets, security) | NEW | Build | M | High | P1 |
| T-82 | BTCPay invoices wired into donation flow + campaign pages | NEW | Build | M | High | P1 |
| T-84 | JP page localization (Japanese) | NEW | Build | L | High | P1 |
| T-85 | JP audience partner / on-camera advocate | NEW | Explore | M–L | High | P1 |
| T-73 | Leleka: build Slack agent on reconciled data layer (shares T-01 data) | NEW | Build | L–XL | Med | P1 |
| T-74 | Leleka: review Zapier-Sniffer overlap after T-70; retire only if use cases are covered (shadow-run first) | NEW | Explore | S–M | Low | P1 |
| T-78 | UX/UI refresh: checkout, forms, donor journey | NEW | Build | M–L | Med | P1 |
| T-79 | Guest checkout (buy/donate without account) | NEW | Build | L | Med | P1 |
| T-80 | Post-purchase registration prompt for physical products (dep T-26) | NEW | Build | M | Med | P1 |
| T-83 | Crypto reconciliation into dashboard/reporting (links T-03/T-44) | NEW | Build | S–M | Med | P1 |
| T-88 | Access register: systems × people × owners (from the §5.2 system list) | NEW | Build | M | Med | P1 |
| T-89 | Access policy: least privilege, system owners, review cadence | NEW | Build | S–M | Med | P1 |
| T-90 | Offboarding checklist: Google Workspace/Drive/sheets, CRM, donation accounts, Slack, CMS, postal, email/video, devices | NEW | Build | S–M | Med | P1 |
| T-91 | Periodic access review + removal (quarterly + after each departure) | NEW | Run | S–M/quarter | Med | P1 |
| T-94 | Unit feedback register: single place for all unit feedback (unit, delivery, date, evidence links, need status) | NEW | Build | S–M | Med | P1 |
| T-95 | One-off consolidation: gather existing scattered unit feedback (CRM, email, messaging, videos/photos) into the register | NEW | Build | M | Med | P1 |
| T-96 | Standing capture: route post-delivery follow-up (3.4/11-day) and incoming unit feedback into the register | NEW | Build | S–M | Med | P1 |
| T-98 | Allocation input: approval lead reviews need status at unit approval + campaign prioritization — satisfied units deprioritized, funds follow remaining need | NEW | Run | S–M/cycle | Med | P1 |
| T-67 | Repeat-allocation gate: refreshed need verification required before any repeat vehicle allocation | NEW | Run | S–M/cycle | Med | P1 |

## P2 — Later

| ID | Task | § | Type | Time | Donation | P |
| --- | --- | --- | --- | --- | --- | --- |
| T-48 | Vehicle-document extraction (VIN, year, make, model from images) | 7.3 | Build | L | Low | P2 |
| T-49 | Unit-document generation from templates at convoy assignment | 7.3 | Build | L | Med | P2 |
| T-50 | Request-video intake directly into CRM workflow | 7.3 | Build | M | Med | P2 |
| T-51 | Initial unit form collection + review | 3.2 | Run | S | Low | P2 |
| T-52 | Coded detailed-application invitations | 3.2 | Run | S | Low | P2 |
| T-53 | Monthly application-code rotation (automate if possible) | 3.2 | Automate | S–M | Low | P2 |
| T-54 | CRM deal QA + language cleanup on generated records | 3.2 | Run | S | Low | P2 |
| T-55 | Intake spreadsheet upkeep | 3.2 | Run | S | Low | P2 |
| T-56 | Allocation register + spreadsheet upkeep | 3.3 | Run | S/convoy | Med | P2 |
| T-57 | Convoy planning (2 drivers/vehicle, travel, lodging, security) | 3.3 | Run | M/convoy | Med | P2 |
| T-58 | Vehicle data + document transfer to allocation workflow | 3.3 | Run | S/vehicle | Med | P2 |
| T-59 | Unit documents preparation (2–3 per vehicle at assignment) | 3.4 | Run | S–M/vehicle | Med | P2 |
| T-60 | Content follow-up completion (11-day action) → mark deal won | 3.4 | Run | S/deal | Low | P2 |
| T-61 | Consolidate website/professional + social reporting | 2.2 | Build | M | Med | P2 |
| T-62 | Phone-number collection where postal service requires it | 4.2 | Run | S | Low | P2 |
| T-63 | Patch inventory discipline (campaign-by-campaign, storage limits) | 4.3 | Run | S | Med | P2 |
| T-64 | Onboarding checklist (contract, device, access, introductions, walkthrough) | 5.1 | Build | S–M | Low | P2 |
| T-65 | Handover/thank-you content reused for recognition + fundraising | 2.1 | Run | S | Med | P2 |
| T-86 | JP international marketing campaign (after T-85 secures partner) | NEW | Run | L | High | P2 |
| T-92 | Deprovisioning audit trail + dormant-account alerts | NEW | Build | M | Med | P2 |
| T-93 | Emergency lockout procedure (compromise or hostile departure) | NEW | Explore | S–M | Med | P2 |
| T-97 | Unit need-status model + refresh cadence (active need / partially met / fully met / unknown) | NEW | Explore | S–M | Med | P2 |
| T-99 | Missing-feedback sweep + monthly unit-needs summary for campaign planning | NEW | Run | S/mo | Low | P2 |

## P3 — Backlog / exploratory

| ID | Task | § | Type | Time | Donation | P |
| --- | --- | --- | --- | --- | --- | --- |
| T-66 | Multi-campaign donor basket (needs stock visibility + packing process) | 7.2 | Build | XL | Med | P3 |
| T-68 | Internal recording/transcription tooling assessment (sensitive meetings) | 5.4/7.3 | Explore | M | Low | P3 |
| T-69 | Specialist platform-support request path | 5.4 | Run | S | Low | P3 |

## Notes

- P0 includes both new work and steady-state revenue operations (marked Run) — the fundraising engine must keep running while the build tracks proceed.
- Donation influence is judged against the manual's own framing: donor experience is the primary automation target; the dashboard is the immediate reporting requirement; tax-deductible expansion is the strategic programme.
- Section 6 handoffs and Section 5.4 constraints are process requirements, not standalone tasks; they are embedded in the tasks above.
- **16.OCT.2026 stakeholder additions (T-70–T-86):** Leleka, the new Slack AI agent (stork — Ukraine's national bird, symbol of home and return; its overlap with the Zapier "Sniffer" is reviewed at T-74, with a decision gate after T-70 and retirement only if use cases are covered), TypeForm/payment/product-flow streamlining, eCommerce guest checkout + registration prompt, BTCPay Server crypto integration, and JP localization + international marketing. Flagged "very important"; rated on the same three axes.
- Leleka should be built on the same reconciled data layer as the dashboard (T-01) to avoid duplicate integrations; it must also satisfy the sensitive-data review already required in 5.4 (cf. T-68).
- BTCPay adds a first-class crypto route (4.1) — wire it into reconciliation (T-03/T-44) from day one; crypto is generally not tax-deductible, so keep it separate from US-channel reporting.
- TypeForm elimination is the front-end half of the primary automation (7.2, T-06) — do the T-75 mapping before the T-77 build.
- JP localization (T-84) can proceed ahead of partner search; per 2.3, hold dedicated campaign spend until T-85 secures an audience partner/advocate.
- **16.OCT.2026 access-control addition (T-87–T-93):** immediate audit + revoke first (T-87); register, policy, offboarding and periodic review (T-88–T-91) as the sustained process; audit trail and emergency lockout as follow-ons. Note: many core records live in Google spreadsheets (intake, fulfillment, allocation) — revocation must explicitly cover them; the offboarding checklist is the counterpart to the §5.1 onboarding steps.
- **16.OCT.2026 unit-feedback addition (T-67, T-94–T-99):** centralize ALL receiving-unit feedback (T-94–T-96), model need status (T-97), and feed it into approval/allocation so satisfied units are deprioritized and future help targets remaining need (T-98–T-99), with a hard gate before repeat allocations (T-67). Completeness matters: a unit that has told us it no longer needs vehicles should never be funded again by default. Feedback capture rides on the §3.4 content follow-up; usable photos/video also feed donor content (T-65).
