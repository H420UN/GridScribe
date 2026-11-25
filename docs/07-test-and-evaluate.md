<img src="../assets/brand/logo/wsp-logo-red.png" alt="WSP" height="28">

[Home](../README.md) › Step 7

# Step 7 — Test, do not just trust

**About 3 minutes for a first pass; finish during review or afterwards.** Step 6 and this first pass share the final five-minute build stage. All eight core tests plus citation inspection will often need longer; divide them between pairs.

1. Open the [test questions](../prompts/test-questions.md). Start with **1, 3, 4 and 5**, one per pair if short of time. Keep the hidden expected behaviours closed.
2. For each answer, open **every requirement's citation**. Check document number, edition, Current/Superseded/Draft status, clause and the actual number. Compare against the original under [the library](../data/library/), not just another model summary.
3. Ask question 7 to draft Section 4. Paste the [template](../templates/design-basis-report-section4.md) into the question if needed; it is not an extra knowledge source. It needs all eight rows.
4. Run questions 2, 6 and 8, then score the result using the [checklist](../evaluation/student-checklist.md). For question 6, use a fresh chat so the grounding test is not only parroting an earlier refusal.
5. If an answer misses, inspect the retrieved chunks. Were the right edition and amendment present? Tighten the [instructions](../prompts/gridscribe-instructions.md), save, start a fresh chat and rerun the **same** question. Record before/after, not just your favourite result.

> [!TIP]
> Give your neighbour one claim to verify. They should find the exact clause without needing to trust your explanation.

The [four bonus questions](../prompts/test-questions.md#bonus-questions) probe the **same scenario**, not extra scenarios.

**Expected result:** an eight-row draft table, evidence checks recorded and a score you can explain. Missing evidence is a valid result, not a reason to invent a number.

**If it fails:** wrong answer with a good-looking citation → open the original and classify retrieval versus reasoning failure. No relevant chunk → test in Search explorer. See [troubleshooting](troubleshooting.md).

---
[← Previous](06-connect-and-ask-gridscribe.md) · [Home](../README.md) · [Next →](08-optional-rag-in-code.md)

WSP AI Accelerator · UoC Insight Day 2026
