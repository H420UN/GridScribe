<img src="../assets/brand/logo/wsp-logo-red.png" alt="WSP" height="28">

[Home](../README.md) › Facilitator › Run sheet

# Beyond the data: how AI really works inside an engineering firm

**GridScribe · Wednesday 25 November 2026 · WSP Cambridge · 13:50–14:35**

Facilitator: **Haroun Abdul Azis**, AI Engineer, WSP AI Accelerator team. Audience: about nine first- to third-year Cambridge engineering students. Assume no Azure experience and no existing Azure accounts.

## Before students arrive

- [ ] Complete the [dry run and backup preparation](backup-plan.md) on 22–23 November.
- [ ] Open the repository home page, portal tabs, [test questions](../prompts/test-questions.md) and a working prepared GridScribe.
- [ ] Keep [answer key](answer-key.md) and [walkthrough](solution-walkthrough.md) off the student screen until review.
- [ ] Have three pairs plus one group of three available for nine students; one account owner operates each browser, with no credential sharing.
- [ ] Leave space for students to enter verification details privately.
- [ ] Check the room clock. Account creation is part of the 25 minutes, not a pre-session task.

## Slide order and opening timings

| Slide | Title / cue | Opening slot |
| --- | --- | --- |
| 1 | Beyond the data: how AI really works inside an engineering firm | 13:50:00–13:50:15 |
| 2 | Agenda | 13:50:15–13:50:30 |
| 3 | About me | 13:50:30–13:51:15 |
| 4 | Two kinds of AI engineer | 13:51:15–13:52:00 |
| 5 | My projects | 13:52:00–13:52:50 |
| 6 | AI Accelerator team | 13:52:50–13:53:40 |
| 7 | Day to day | 13:53:40–13:54:30 |
| 8 | Your turn: build GridScribe | 13:54:30–13:55:00 |
| 9 | Step 0: get your free Azure account — two routes, five sign-up steps | 13:55–13:58 |
| 10 | Step 0: set up your workspace in the portal | 13:58–14:00 |
| 11 | Your mission: brief, RAG, services and six timed steps | **14:00–14:20; leave on screen** |
| 12 | Solution review | 14:20–14:25 |
| 13 | Certificates to bridge into AI | 14:25, a short signpost before questions |
| 14 | Questions and contact | 14:25–14:35 |

Slides **3–7 total exactly four minutes**. Talk about approved project examples only; do not improvise real client details. Slide 11's mission is still the single Fen Edge scenario.

## Minute-by-minute

| Clock | Slide | What I say / do |
| --- | --- | --- |
| 13:50–13:51 | 1–3 | "Welcome. We'll build an assistant, then try to catch it out." Brief agenda, then introduce my role. |
| 13:51–13:52 | 3–4 | "Frontier engineers train models. Applied AI engineers build WITH models." |
| 13:52–13:53 | 5–6 | Give one approved, non-sensitive example of connecting models to useful workflows; introduce the team. |
| 13:53–13:54 | 6–7 | "A lot of the work is data, testing and checking—not asking for a clever paragraph." |
| 13:54–13:55 | 7–8 | Finish day-to-day by :30. "Your turn: one fictional energy hub, a mixed library, a report to check." |
| 13:55–13:56 | 9 | Start account creation. "Personal account, never work. Try Students first; no card. Free account is the alternative." |
| 13:56–13:57 | 9 | Walk the five sign-up steps; keep verification private. Point to the offer comparison. |
| 13:57–13:58 | 9 | Apply the two-minute verification rule. Pair anyone blocked; never suggest upgrading to pay-as-you-go. |
| 13:58–13:59 | 10 | "Check Active subscription; create the workshop resource group. Same account in both portals." |
| 13:59–14:00 | 10 | Download/unzip the repo; launch Search early. At 14:00 anyone still blocked pairs up or joins my demo. |
| 14:00–14:01 | 11 | Start storage creation: Standard, LRS, Hot, existing group. Ask pairs to split operator/evidence-checker roles. |
| 14:01–14:02 | 11 | Create private `library`. "Private container, not private networking; no public document access." |
| 14:02–14:03 | 11 | Upload standards and WSP publications using the virtual-folder field. |
| 14:03–14:04 | 11 | Upload project files; count 19 + 10 + 7. Flat names are fine if needed; no duplicate copies. |
| 14:04–14:05 | 11 | Check Search deployment. Free if the tested route works; agreed Basic only with its price understood. |
| 14:05–14:06 | 11 | Fix one naming/region issue quickly, otherwise use pairs. Check required keys/roles for the tested route. |
| 14:06–14:07 | 11 | "Our index will be `gridscribe-index`. A service and an index are different things." |
| 14:07–14:08 | 11 | Create Foundry project in the same group; keep New Foundry on. |
| 14:08–14:09 | 11 | Deploy the approved current small chat model as `gridscribe-chat`. |
| 14:09–14:10 | 11 | Deploy `text-embedding-3-small`; explain that embeddings do not write answers. |
| 14:10–14:11 | 11 | Confirm both deployments Succeeded. Zero quota → approved alternative or pairs/demo, not a quota-request detour. |
| 14:11–14:12 | 11 | Import data › Blob › RAG; choose `library` without a folder filter. |
| 14:12–14:13 | 11 | Select embeddings. "Chunk, embed, index." Skip OCR/images; keep the tested ordinary-hybrid configuration. |
| 14:13–14:14 | 11 | Check source mapping and index name; create once. Read indexer execution details. |
| 14:14–14:15 | 11 | Search explorer test; check actual chunks and current/draft status. Rerun after timeout only when allowed. |
| 14:15–14:16 | 11 | Connect the tested direct Search tool to the new GridScribe agent; paste instructions. |
| 14:16–14:17 | 11 | Ask minimum spacing; "Open the citation. Does it say what the answer claims?" |
| 14:17–14:18 | 11 | Divide core tests 1/3/4/5 between pairs. Do not reveal answers yet. |
| 14:18–14:19 | 11 | Ask for Section 4 with the template. Inspect editions and missing evidence; score first pass. |
| 14:19–14:20 | 11 | "Save one success and one miss. Stop provisioning now." Slow pairs join the prepared retrieval results. |
| 14:20–14:21 | 12 | Reveal issue 1: the old BESS rule and outdated note; current rule and amendment. |
| 14:21–14:22 | 12 | Reveal issue 2: 4.6% is above 4%; don't use the old 5% or DC 1.5% rule. |
| 14:22–14:23 | 12 | Reveal issue 3: a newer draft is not a requirement; 12 m passes the current 10 m. |
| 14:23–14:24 | 12 | Reveal issue 4: "No source found in the library." Pressure is not evidence. |
| 14:24–14:25 | 12 | Check the compliant distractors, then show how better instructions and better retrieval differ. |
| 14:25–14:26 | 13–14 | Brief certificates/learning-path signpost, then open questions. "A credential helps structure learning; tested work shows the skill." |
| 14:26–14:27 | 14 | Take a question about models versus data; use the two RAG journeys. |
| 14:27–14:28 | 14 | Take an engineering assurance question; distinguish a source citation from professional sign-off. |
| 14:28–14:29 | 14 | Take a cloud/cost question; point to cleanup and credit protection. |
| 14:29–14:30 | 14 | Final Q&A minute. Repeat the key message about checking edition, clause and number. |
| 14:30–14:31 | 14 | Buffer/cleanup: save drafts; open only your workshop resource group. |
| 14:31–14:32 | 14 | Start group deletion; check names carefully. |
| 14:32–14:33 | 14 | Verify deletion or inspect failures. Check for stray Basic Search/Cloud Shell resources. |
| 14:33–14:34 | 14 | Show budget alerts if supported; remind students these are not spending caps. |
| 14:34–14:35 | 14 | Confirm each account owner's cleanup; share repo/help route and thank the group. |

**Totals:** intro 5 min; hands-on 25 min (first 5 account/workspace); review 5 min; Q&A 5 min; buffer 5 min. Protect the review: use the backup rather than sacrificing it to provisioning.

The [optional code extension](../docs/08-optional-rag-in-code.md) is not part of this clock. No Cloud Shell during the core lab.

> [!NOTE]
> TODO (facilitator): verify in dry run — rehearse slides 3–7 in four minutes, test the 25-minute build with a novice, and verify slide 13's live certification/learning-path names and slide 14's approved contact details. If the build exceeds the budget, announce the paired/demo mode rather than cutting the review or safety cleanup.

---
[← Previous](backup-plan.md) · [Home](../README.md) · [Next →](answer-key.md)

WSP AI Accelerator · UoC Insight Day 2026
