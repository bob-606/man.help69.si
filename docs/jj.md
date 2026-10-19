# JJ's Task List

Task list for the Systems Builder role — 41 tasks. Interactive view:
[`jj.html`](jj.html) — sort, filter, and expand any task for a plain-words explanation.

## Legend

- **Time** — S (<1 day) · M (1–5 days) · L (1–3 weeks) · XL (>1 month).
- **Donation impact** — High: directly grows or protects income/donor experience · Med: supports it indirectly · Low: internal efficiency only.
- **Priority** — P0 (highest) → P3 (lowest).

## Tasks

| ID | Task | Time | Donation impact | P |
| --- | --- | --- | --- | --- |
| JJ-01 | Leleka (Slack AI agent): use-case catalogue + data-source inventory | S–M | Med | P0 |
| JJ-02 | Leleka (Slack AI agent): platform evaluation — Hermes Agent vs alternatives | M | Med | P0 |
| JJ-03 | Map the current payment + goods-receipt flow | S–M | High | P0 |
| JJ-04 | TypeForm decision: integrate vs eliminate | S | High | P0 |
| JJ-05 | Build the shared reporting dashboard | L | High | P0 |
| JJ-06 | Donation-account feeds into the dashboard | M | High | P0 |
| JJ-07 | Bank + crypto records into the reconciliation view | M | Med | P0 |
| JJ-08 | Web analytics + social feeds into the dashboard | M | Med | P0 |
| JJ-09 | Subscription reconciliation across donation accounts (protects ~700 donors / ~€70k per month) | M | High | P0 |
| JJ-10 | Automated payment matching to donor, campaign and account | L | High | P0 |
| JJ-11 | Automated benefit-request intake | L | High | P0 |
| JJ-12 | Eligibility rule engine | M–L | High | P0 |
| JJ-13 | Replace donation-proof screenshots with reliable payment matching | M–L | Med | P1 |
| JJ-14 | Reusable, editable donor shipping profile | L | Med | P1 |
| JJ-15 | Selection catalogue update on campaign completion | S–M | Med | P1 |
| JJ-16 | Recognition list sync (website + video channel) | M | Med | P1 |
| JJ-17 | Auto-link handover video to vehicle/message/donor | L | High | P1 |
| JJ-18 | Auto-route uploads to subtitle contributors; hold unlinked files | M | High | P1 |
| JJ-19 | Auto-send donor email after subtitles | M | High | P1 |
| JJ-20 | Packing list + postal CSV generation (worldwide + US) | L | Med | P1 |
| JJ-21 | Stock-readiness gating | M | Med | P1 |
| JJ-22 | Flag unit-patch bonus vs 3-patch limit overlaps | S–M | Low | P1 |
| JJ-23 | Leleka (Slack AI agent): data access, permissions, sensitive-data review | M | Med | P0 |
| JJ-24 | Leleka (Slack AI agent): build the agent on the reconciled data layer | L–XL | Med | P1 |
| JJ-25 | Leleka (Slack AI agent): Zapier bot overlap review | S–M | Low | P1 |
| JJ-26 | BTCPay Server deployment (hosting, wallets, security) | M | High | P3 |
| JJ-27 | BTCPay crypto invoices in the donation flow + campaign pages | M | High | P3 |
| JJ-28 | WalletConnect integration | M | High | P3 |
| JJ-29 | Streamlined donation → benefits → payment → product flow | L | High | P0 |
| JJ-30 | Vehicle-document extraction (VIN, year, make, model) | L | Low | P0 |
| JJ-31 | Unit-document generation at convoy assignment | L | Med | P0 |
| JJ-32 | Request-video intake into the CRM workflow | M | Med | P0 |
| JJ-33 | Unit-application invite-code rotation | S–M | Low | P0 |
| JJ-34 | Deprovisioning audit trail + dormant-account alerts | M | Med | P0 |
| JJ-35 | Emergency lockout procedure | S–M | Med | P0 |
| JJ-36 | Secure database infrastructure for sensitive personal data | L | Med | P0 |
| JJ-37 | Social media: channel + access inventory (platforms, brand accounts, publishing access) | S–M | Med | P1 |
| JJ-38 | Social media: publishing queue — schedule + cross-post with a marketing approval step | L | Med | P1 |
| JJ-39 | Social media: campaign launch kit — captions, per-channel formats, tagged links | M | High | P1 |
| JJ-40 | Social media: auto-clips + captions from existing request/handover videos | L | Med | P2 |
| JJ-41 | Social media: channel attribution — tagged links → donations in the dashboard | M | High | P1 |

## In plain words

- **JJ-01** — Collect what people actually want to ask the agent, and check which of that data already exists — so the build targets real questions.
- **JJ-02** — Choose the platform to build on (Hermes Agent vs alternatives), including how it connects to Slack and what today's Zapier bot cannot do.
- **JJ-03** — Draw today's path from a payment to a delivered product, including every tool and handoff in between (TypeForm, donation platform, postal).
- **JJ-04** — Decide whether TypeForm stays (plugged into the new flow) or is dropped.
- **JJ-05** — One place for reporting: a single reporting period, clear currency rules, payment account and payment method kept apart, refresh times shown, missing data flagged.
- **JJ-06** — Feed campaign receipts, totals and one-time vs recurring splits from the donation accounts into the dashboard.
- **JJ-07** — Add bank and crypto records so every incoming payment shows up in the reconciliation view.
- **JJ-08** — Add website traffic and social media numbers to the dashboard.
- **JJ-09** — ~700 recurring donors (~€70,000/month) sit on the legacy account; this flags any failed or dropped recurring payments early.
- **JJ-10** — Match each payment to the right donor, campaign and donation account automatically — no manual lookups.
- **JJ-11** — Reuse saved donor details, capture what they choose, and generate the fulfillment record automatically.
- **JJ-12** — Apply the benefit rules automatically: 3-patch limit per shipment, €750+ bonus patch, vehicle messages from €1,500 (max 4 per vehicle), recurring tiers.
- **JJ-13** — Retire the practice of donors sending payment screenshots — reliable matching (JJ-10) becomes the proof.
- **JJ-14** — One saved shipping profile per donor that they can edit and every fulfillment reuses.
- **JJ-15** — Update the selection catalogue as soon as a campaign finishes.
- **JJ-16** — Keep the website and video-channel recognition lists in sync with active donors.
- **JJ-17** — Match every uploaded handover video to its vehicle, its message and its donor automatically.
- **JJ-18** — Route each upload to the right subtitle contributor automatically, and hold back any file that can't be matched to its vehicle/message/donor.
- **JJ-19** — Email the donor the correct subtitled video, with duplicate protection and a retry path if sending fails.
- **JJ-20** — Generate the packing list and postal export files (worldwide and US formats) for each batch.
- **JJ-21** — Hold a campaign batch until its patches are actually in stock.
- **JJ-22** — Flag cases where the unit-patch bonus conflicts with the 3-patch limit, for the shipping team to review.
- **JJ-23** — Decide exactly what data the agent may read and under which privacy rules, before anything is built.
- **JJ-24** — Build the agent on the same data as the dashboard (JJ-05) — one shared pipeline, not two.
- **JJ-25** — Run the agent and the current bot side by side; retire the bot only once the agent covers all its use cases.
- **JJ-26** — Set up the self-hosted BTCPay server: hosting, wallets, security.
- **JJ-27** — Wire BTCPay's crypto invoices into the normal donation flow and the campaign pages.
- **JJ-28** — Let donors connect a wallet to give via the crypto route.
- **JJ-29** — Wire the intake, eligibility and payment-matching work into one smooth path: donation → benefit selection → payment → product (depends on JJ-11, JJ-12, JJ-13).
- **JJ-30** — Read VIN, year, make and model off vehicle-document images automatically.
- **JJ-31** — Generate unit documents from templates at convoy assignment.
- **JJ-32** — Enter request videos straight into the CRM workflow.
- **JJ-33** — Automate the monthly rotation of the unit-application invite code.
- **JJ-34** — Keep an audit trail of account removals and alert on dormant (unused) accounts.
- **JJ-35** — A ready procedure to lock accounts fast when there's a compromise or a hostile departure.
- **JJ-36** — Set up secure storage for sensitive personal data: hosting, encryption, access control.
- **JJ-37** — List every social platform and brand account in use, who controls each login, and what publishing access exists — so the pipeline is built on real access, not assumptions.
- **JJ-38** — One queue where a post is written once, scheduled, and published to every channel — with a Marketing approval step before anything goes live.
- **JJ-39** — Generate the per-campaign posting kit from the campaign brief: caption variants, correctly sized images, and campaign links tagged per channel.
- **JJ-40** — Cut short vertical clips with captions from videos we already have (the video pipeline, JJ-17–JJ-19), so existing footage becomes social content without manual editing.
- **JJ-41** — Tag every campaign link per channel so the dashboard shows which platform actually brought donations — JJ-08 brings platform numbers in; this connects them to money.
