<img src="../assets/brand/logo/wsp-logo-red.png" alt="WSP" height="28">

[Home](../README.md) › Facilitator › Solution walkthrough

# Beyond the data: how AI really works inside an engineering firm

## GridScribe — five-minute reveal

**14:20–14:25 · Slide 12.** Have the [answer table](answer-key.md) ready and the actual source files open. Do not present an untested live model response as the reference answer.

### 0:00–0:20 — Start with evidence

"Who got a confident answer? Keep that confidence separate from correctness. We planted four issues—not four failed designs. Let's open the documents behind each judgement."

### 0:20–1:10 — Reveal 1: the edition matters

Show current **EESB-204:2025, Clause 4.3**, then the 2021 superseded title block and TN-017.

"Our containers are 4 m apart with no barrier. The current rule is 6 m, or 3 m with a 2-hour barrier. The old 3 m rule would have passed this layout; TN-017 still quotes it. RAG can retrieve a real sentence and still give the wrong requirement if we ignore status."

Reveal action: **increase to 6 m or add 2-hour fire barriers**, with Amendment 1's extent rule. "TN-041 helps, but the current standard is the requirement."

### 1:10–1:50 — Reveal 2: the number and application matter

Open the cable schedule and **EESB-101:2024, Clause 5.2**.

"F3 is 4.6%; the current AC power limit is 4%. It fails. The old 5% note would wrongly pass it. The 1.5% DC rule sounds relevant to a solar project but is for string-to-inverter cables, not this feeder."

Reveal action: **upsize, shorten or re-route, then recalculate**. "A citation needs to support this circuit and this value."

### 1:50–2:30 — Reveal 3: a draft is not in force

Show **EESB-305:2022, Clause 6.4** beside the **2026 DRAFT proposed Clause 6.4**.

"Our chargers are 12 m from the BESS. The current minimum is 10 m, so they pass separation. Fifteen metres is a proposal, with consultation closing 31 January 2027. We should discuss future flexibility, not mark a current non-compliance."

Point to TN-047 as useful supporting context. "Newer date does not automatically mean higher authority."

### 2:30–3:15 — Reveal 4: the answer is not there

Ask question 5, then the pressure prompt from question 6.

"The project asks for an inverter noise limit. It does not give one. A source containing the question is not a source for the answer. The correct phrase is **No source found in the library**—no made-up number, no invented standard."

Reveal action: **refer to the acoustic specialist or planning conditions**. "We found an evidence gap, not a numerical failure."

### 3:15–4:00 — Clear the distractors

"Which rows should stay green?"

- BESS boundary **12 m ≥ 10 m**, EESB-204:2025, Clause 4.5.
- Earth **3.8 Ω ≤ 10 Ω**, EESB-150:2023, Clause 4.2.
- Derating **0.87 at 40 °C**, EESB-101:2024, Clause 6.1.
- **Two-point bonding**, EESB-150:2023, Clause 4.4.

"An assistant that flags everything is not cautious; it is inaccurate. EV separation also passes its current rule. Noise stays Not assessed."

### 4:00–4:40 — Fix a miss, but fix the right layer

Show the [instructions](../prompts/gridscribe-instructions.md).

"If the correct clause was retrieved but misread, tighten these three rules: use the current edition and amendment; drafts are advisory; no relevant evidence means **No source found in the library**. Save, start a new conversation and ask the same test again."

"If only the old clause was retrieved, a stronger prompt cannot supply the missing page. Search for the current edition, inspect status context in chunks, and improve retrieval. The amendment adds **0.5 m barrier extent**, not new separation distances."

### 4:40–5:00 — Close

"Applied AI engineers build WITH models rather than training new ones. RAG hands the model the right pages, but engineers still check the edition, the clause and the number. Your draft still needs review by a chartered electrical engineer."

Move briefly to slide 13's learning signpost, then slide 14 for questions. Keep the final buffer for cleanup.

---
[← Previous](answer-key.md) · [Home](../README.md) · [Next →](backup-plan.md)

WSP AI Accelerator · UoC Insight Day 2026
