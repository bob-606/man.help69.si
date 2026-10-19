# JJ's Task List

Task list for the Systems Builder role — 11 main tasks with 41 subtasks. Interactive view:
[`jj.html`](jj.html) — sort, filter, and expand any task for a plain-words explanation.

## Legend

- **Time** — S (<1 day) · M (1–5 days) · L (1–3 weeks) · XL (>1 month).
- **Donation impact** — High: directly grows or protects income/donor experience · Med: supports it indirectly · Low: internal efficiency only.
- **Priority** — P0 (highest) → P3 (lowest).

## Tasks

### JJ-01 · Leleka (Slack AI agent)
A Slack assistant that answers operational questions from our data. Evaluated and data-safety checked first; built on the dashboard's data layer; the current Zapier bot is retired only if the agent covers its jobs.
Handoff: in — data questions from every team · out — answers in Slack.

| ID | Subtask | Time | Donation impact | P |
| --- | --- | --- | --- | --- |
| JJ-01.1 | Use-case catalogue + data-source inventory | S–M | Med | P0 |
| JJ-01.2 | Platform evaluation — Hermes Agent vs alternatives | M | Med | P0 |
| JJ-01.3 | Data access, permissions, sensitive-data review | M | Med | P0 |
| JJ-01.4 | Build the agent on the reconciled data layer | L–XL | Med | P1 |
| JJ-01.5 | Zapier bot overlap review (retire only if covered) | S–M | Low | P1 |

In plain words:
- **JJ-01.1** — Collect what people actually want to ask the agent, and check which of that data already exists — so the build targets real questions.
- **JJ-01.2** — Choose the platform to build on (Hermes Agent vs alternatives), including how it connects to Slack and what today's Zapier bot cannot do.
- **JJ-01.3** — Decide exactly what data the agent may read and under which privacy rules, before anything is built.
- **JJ-01.4** — Build the agent on the same data as the dashboard (JJ-03) — one shared pipeline, not two.
- **JJ-01.5** — Run the agent and the current bot side by side; retire the bot only once the agent covers all its use cases.

### JJ-02 · Flow mapping & tool decisions
Short discovery first: map how money and products move today, and settle what happens to TypeForm — before any automation is built.
Handoff: in — process knowledge from DonorOps, MilOps and the website developer · out — the flow map and the TypeForm decision for every later build.

| ID | Subtask | Time | Donation impact | P |
| --- | --- | --- | --- | --- |
| JJ-02.1 | Map the payment + goods-receipt flow | S–M | High | P0 |
| JJ-02.2 | TypeForm decision: integrate vs eliminate | S | High | P0 |

In plain words:
- **JJ-02.1** — Draw today's path from a payment to a delivered product, including every tool and handoff in between (TypeForm, donation platform, postal).
- **JJ-02.2** — Decide whether TypeForm stays (plugged into the new flow) or is dropped.

### JJ-03 · Reporting dashboard & data layer
One shared dashboard fed from every money and reach source — and the same reconciled data layer later feeds the Slack agent.
Handoff: in — donation-platform, bank, crypto, analytics and social feeds · out — the weekly dashboard the core team reviews.

| ID | Subtask | Time | Donation impact | P |
| --- | --- | --- | --- | --- |
| JJ-03.1 | Build the shared reporting dashboard | L | High | P0 |
| JJ-03.2 | Donation-account feeds into the dashboard | M | High | P0 |
| JJ-03.3 | Bank + crypto records into the reconciliation view | M | Med | P0 |
| JJ-03.4 | Web analytics + social feeds into the dashboard | M | Med | P0 |

In plain words:
- **JJ-03.1** — One place for reporting: a single reporting period, clear currency rules, payment account and payment method kept apart, refresh times shown, missing data flagged.
- **JJ-03.2** — Feed campaign receipts, totals and one-time vs recurring splits from the donation accounts into the dashboard.
- **JJ-03.3** — Add bank and crypto records so every incoming payment shows up in the reconciliation view.
- **JJ-03.4** — Add website traffic and social media numbers to the dashboard.

### JJ-04 · Payment matching & recurring-donation protection
Every incoming payment matched to its donor — and the ~€70k/month recurring base kept from slipping away unnoticed.
Handoff: in — payment records and donor records · out — verified matches for the dashboard and fulfillment, and early alerts for DonorOps.

| ID | Subtask | Time | Donation impact | P |
| --- | --- | --- | --- | --- |
| JJ-04.1 | Subscription reconciliation across donation accounts (protects ~700 donors / ~€70k per month) | M | High | P0 |
| JJ-04.2 | Automated payment matching to donor, campaign and account | L | High | P0 |
| JJ-04.3 | Replace donation-proof screenshots with reliable payment matching | M–L | Med | P1 |

In plain words:
- **JJ-04.1** — ~700 recurring donors (~€70,000/month) sit on the legacy account; this flags any failed or dropped recurring payments early.
- **JJ-04.2** — Match each payment to the right donor, campaign and donation account automatically — no manual lookups.
- **JJ-04.3** — Retire the practice of donors sending payment screenshots — reliable matching (JJ-04.2) becomes the proof.

### JJ-05 · Donor fulfillment automation
The core donor workflow: requests in, benefit rules applied, records generated — plus the lists and profiles around it. Ends with the end-to-end streamlined flow.
Handoff: in — donors' benefit choices · out — fulfillment records for MilOps packing and shipping.

| ID | Subtask | Time | Donation impact | P |
| --- | --- | --- | --- | --- |
| JJ-05.1 | Automated benefit-request intake | L | High | P0 |
| JJ-05.2 | Eligibility rule engine | M–L | High | P0 |
| JJ-05.3 | Reusable, editable donor shipping profile | L | Med | P1 |
| JJ-05.4 | Selection catalogue update on campaign completion | S–M | Med | P1 |
| JJ-05.5 | Recognition list sync (website + video channel) | M | Med | P1 |
| JJ-05.6 | Streamlined donation → benefits → payment → product flow | L | High | P0 |

In plain words:
- **JJ-05.1** — Reuse saved donor details, capture what they choose, and generate the fulfillment record automatically.
- **JJ-05.2** — Apply the benefit rules automatically: 3-patch limit per shipment, €750+ bonus patch, vehicle messages from €1,500 (max 4 per vehicle), recurring tiers.
- **JJ-05.3** — One saved shipping profile per donor that they can edit and every fulfillment reuses.
- **JJ-05.4** — Update the selection catalogue as soon as a campaign finishes.
- **JJ-05.5** — Keep the website and video-channel recognition lists in sync with active donors.
- **JJ-05.6** — Wire everything above into one smooth path: donation → benefit selection → payment → product (depends on JJ-04.3, JJ-05.1, JJ-05.2).

### JJ-06 · Video pipeline
From uploaded handover video to the donor's inbox: matched to donor and vehicle, sent for subtitles, delivered by email.
Handoff: in — raw handover videos from MilOps · out — subtitled videos emailed to donors.

| ID | Subtask | Time | Donation impact | P |
| --- | --- | --- | --- | --- |
| JJ-06.1 | Auto-link handover video to vehicle/message/donor | L | High | P1 |
| JJ-06.2 | Auto-route uploads to subtitle contributors; hold unlinked files for coordination | M | High | P1 |
| JJ-06.3 | Auto-send donor email after subtitles | M | High | P1 |

In plain words:
- **JJ-06.1** — Match every uploaded handover video to its vehicle, its message and its donor automatically.
- **JJ-06.2** — Handover videos must reach subtitle contributors before they go to donors — today that hand-off is manual. This task routes each upload to the right contributor automatically, and holds back any file that can't be matched to its vehicle/message/donor.
- **JJ-06.3** — Email the donor the correct subtitled video, with duplicate protection and a retry path if sending fails.

### JJ-07 · Shipping & packing automation
Packing documents and readiness checks straight from the system, so batches ship correctly.
Handoff: in — fulfillment records and stock status from MilOps · out — packing lists and postal files for the shipping team.

| ID | Subtask | Time | Donation impact | P |
| --- | --- | --- | --- | --- |
| JJ-07.1 | Packing list + postal CSV generation (worldwide + US) | L | Med | P1 |
| JJ-07.2 | Stock-readiness gating | M | Med | P1 |
| JJ-07.3 | Flag unit-patch bonus vs 3-patch limit overlaps | S–M | Low | P1 |

In plain words:
- **JJ-07.1** — Generate the packing list and postal export files (worldwide and US formats) for each batch.
- **JJ-07.2** — Hold a campaign batch until its patches are actually in stock.
- **JJ-07.3** — Flag cases where the unit-patch bonus conflicts with the 3-patch limit, for the shipping team to review.

### JJ-08 · Crypto donations (BTCPay)
A self-hosted crypto donation route: server, invoices, wallet connection — not a priority for now.
Handoff: in — donor crypto payments · out — crypto records in reporting, kept separate from US tax receipts.

| ID | Subtask | Time | Donation impact | P |
| --- | --- | --- | --- | --- |
| JJ-08.1 | BTCPay Server deployment (hosting, wallets, security) | M | High | P3 |
| JJ-08.2 | BTCPay crypto invoices in the donation flow + campaign pages | M | High | P3 |
| JJ-08.3 | WalletConnect integration | M | High | P3 |

In plain words:
- **JJ-08.1** — Set up the self-hosted BTCPay server: hosting, wallets, security.
- **JJ-08.2** — Wire BTCPay's crypto invoices into the normal donation flow and the campaign pages.
- **JJ-08.3** — Let donors connect a wallet to give via the crypto route.

### JJ-09 · MilOps document & intake tooling
Automating the internal paperwork for units, vehicles and intake.
Handoff: in — vehicle and unit documents plus application videos from MilOps · out — structured records in the CRM for MilOps.

| ID | Subtask | Time | Donation impact | P |
| --- | --- | --- | --- | --- |
| JJ-09.1 | Vehicle-document extraction (VIN, year, make, model) | L | Low | P0 |
| JJ-09.2 | Unit-document generation at convoy assignment | L | Med | P0 |
| JJ-09.3 | Request-video intake into the CRM workflow | M | Med | P0 |
| JJ-09.4 | Unit-application invite-code rotation | S–M | Low | P0 |

In plain words:
- **JJ-09.1** — Read VIN, year, make and model off vehicle-document images automatically.
- **JJ-09.2** — Generate unit documents from templates at convoy assignment.
- **JJ-09.3** — Enter request videos straight into the CRM workflow.
- **JJ-09.4** — Automate the monthly rotation of the unit-application invite code.

### JJ-10 · Access control & security
Who can access what, what happens when someone leaves — and what to do in an emergency.
Handoff: in — staff changes from Ops · out — audited accounts and a ready emergency-lockout procedure for Ops.

| ID | Subtask | Time | Donation impact | P |
| --- | --- | --- | --- | --- |
| JJ-10.1 | Deprovisioning audit trail + dormant-account alerts | M | Med | P0 |
| JJ-10.2 | Emergency lockout procedure | S–M | Med | P0 |
| JJ-10.3 | Secure database infrastructure for sensitive personal data | L | Med | P0 |

In plain words:
- **JJ-10.1** — Keep an audit trail of account removals and alert on dormant (unused) accounts.
- **JJ-10.2** — A ready procedure to lock accounts fast when there's a compromise or a hostile departure.
- **JJ-10.3** — Set up secure storage for sensitive personal data: hosting, encryption, access control.

### JJ-11 · Social media publishing & enhancement
Campaign and handover content turned into scheduled social posts — with tagged links so each channel's donations are traceable — instead of one-off manual posting.
Handoff: in — campaign material from Marketing, videos and photos from MilOps · out — scheduled posts on every channel, and per-channel reach and donations in the dashboard.

| ID | Subtask | Time | Donation impact | P |
| --- | --- | --- | --- | --- |
| JJ-11.1 | Channel + access inventory (platforms, brand accounts, publishing access) | S–M | Med | P1 |
| JJ-11.2 | Publishing queue: schedule + cross-post with a marketing approval step | L | Med | P1 |
| JJ-11.3 | Campaign launch kit: captions, per-channel formats, tagged links | M | High | P1 |
| JJ-11.4 | Auto-clips + captions from existing request/handover videos | L | Med | P2 |
| JJ-11.5 | Channel attribution: tagged links → donations in the dashboard | M | High | P1 |

In plain words:
- **JJ-11.1** — List every social platform and brand account in use, who controls each login, and what publishing access exists — so the pipeline is built on real access, not assumptions.
- **JJ-11.2** — One queue where a post is written once, scheduled, and published to every channel — with a Marketing approval step before anything goes live.
- **JJ-11.3** — Generate the per-campaign posting kit from the campaign brief: caption variants, correctly sized images, and campaign links tagged per channel.
- **JJ-11.4** — Cut short vertical clips with captions from videos we already have (the same files as JJ-06), so existing footage becomes social content without manual editing.
- **JJ-11.5** — Tag every campaign link per channel so the dashboard shows which platform actually brought donations — JJ-03.4 brings platform numbers in; this connects them to money.
