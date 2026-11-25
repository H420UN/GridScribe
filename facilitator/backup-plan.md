<img src="../assets/brand/logo/wsp-logo-red.png" alt="WSP" height="28">

[Home](../README.md) › Facilitator › Backup plan

# Beyond the data: how AI really works inside an engineering firm

## GridScribe — dry run and backup

**No student arrives with an Azure account.** The primary route (Search **Free** with key-based connections, a Foundry agent with the Azure AI Search tool) follows the controls documented on Microsoft Learn as checked on **13 November 2026**. It still needs one full dry run on fresh subscriptions before the day: sign-up time, quotas and exact button labels vary. The optional Python script is offline-tested only.

## If accounts or services fail

1. After two minutes of stalled verification, offer the alternative eligible free route or pair up. Never ask students to show passwords, card details, verification codes or academic-verification links.
2. Use three pairs and one group of three for nine students if needed. The account owner drives; partners inspect requirements and citations. Do not share accounts.
3. At **14:00**, anyone still blocked joins a working pair or the facilitator's prepared environment. At **14:15**, anyone still provisioning switches to the prepared retrieval/agent demonstration. Keep the 14:20 review.
4. If the room's cloud route fails entirely, project the pre-built GridScribe. Students use the same test questions, source library, report template and checklist. Have them predict the result **before** showing it.
5. If internet fails, use the downloaded library and saved/redacted outputs from the dry run for the same evidence-checking task. Label recorded outputs honestly; do not pretend an offline discussion is a deployed RAG system.

The pre-built environment is the facilitator's approved environment, not a promise that a student offer can create the same services. Do not create organisational resources or share organisational keys to bypass trial restrictions.

## Dry run: 22–23 November (2–3 days before)

- [ ] Start with a **fresh eligible free-trial account**; time sign-up itself.
- [ ] If possible, ask a current eligible student to test **Azure for Students**, without handing over their account.
- [ ] Confirm offer eligibility, university verification, credit and spending protection; no paid upgrade.
- [ ] Validate an allowed common region, non-zero model quota and model lifecycle: default `gpt-5.4-mini`, then `gpt-5.4-nano`, then larger/costlier `gpt-5.1`; embeddings `text-embedding-3-small`. A model being listed does not prove deployability.
- [ ] Confirm `gridscribe-chat` is selectable in a new agent and the Azure AI Search tool can be added to it.
- [ ] Run the Step 5 wizard on Search **Free** with managed identity unticked, embedding kind **Azure OpenAI** and **API key**. Confirm the Foundry resource appears in the Azure OpenAI picker. If it does not, decide and announce **Basic with cost consent** (Step 5 managed-identity route) or pairs before the session.
- [ ] Record the actual Basic regional/currency price, token rates and trial credit used. Do not claim a fixed per-student cost without measurement.
- [ ] Verify all resources and any automatically created dependencies stay in `rg-gridscribe-<initials>`.
- [ ] Time storage creation and all three upload batches; verify 19 + 10 + 7 sources.
- [ ] Confirm wizard output `gridscribe-index` with `chunk`, `title`, `text_vector` (1,536 dimensions) and the added `url` field populated for every chunk.
- [ ] Record all-36-source indexer success, no failures or unexplained warnings, runtime, chunks, index storage and vector memory. If multiple runs are needed, include that in timings.
- [ ] Walk Step 6 exactly as written: connection `gridscribe-search`, **Tools** › **Add** › **Azure AI Search**, hybrid (`vector_simple_hybrid`), top 5. Correct any button label that differs and check citations show file titles.
- [ ] Open private-source citations without making the Blob container anonymous.
- [ ] Run all eight core and four bonus tests; keep redacted outputs, including misses, for the backup demo. Draft the exact eight-row table.
- [ ] Rehearse a novice build. If it exceeds 25 minutes, use paired/demo mode honestly rather than silently dropping account creation or review.
- [ ] Test the optional script in Cloud Shell with **Entra**, then explicit keys, including permission failures and actual index fields.
- [ ] Capture all planned screenshots; redact keys, subscription identifiers, names and verification details.
- [ ] Rehearse slides 3–7 in four minutes; check learning-path/certificate titles and contact details.
- [ ] Delete **everything** created for the dry run and verify deletion. Rebuild only the approved facilitator demonstration that you need for the event; record its owner and cleanup time.

## Complete TODO register

This is the consolidated list of every `TODO (facilitator)` callout left in the pack. Check off the underlying callout as well as this list after a successful test.

| ID | Location | What to verify |
| --- | --- | --- |
| T01 | [README](../README.md) | Fresh free-trial + student full route, 36 files, citations and total timing |
| T02 | [Step 0](../docs/00-get-your-azure-account.md) | Both live sign-up flows, GitHub option, identity screen order and timing |
| T03 | [Step 2](../docs/02-storage-and-upload.md) | Multi-select, Upload to folder and four-minute storage/upload target |
| T04 | [Step 3](../docs/03-create-ai-search.md) | Free service can be created under both offers |
| T05 | [Step 4: quota/models](../docs/04-foundry-and-models.md) | Current non-deprecated models, embeddings, region policy, quotas, tool support and latency |
| T06 | [Step 4: new portal](../docs/04-foundry-and-models.md) | New project shows **Build** › **Agents**; chat deployment selectable for agents |
| T07 | [Step 5: wizard](../docs/05-index-the-library.md) | Foundry resource listed under Azure OpenAI kind with API key; `url` field added and populated |
| T08 | [Step 5: run](../docs/05-index-the-library.md) | All 36 sources succeed in one run; note runtime and chunk count |
| T09 | [Step 6: tool labels](../docs/06-connect-and-ask-gridscribe.md) | Button labels for adding the Search tool and choosing hybrid search; update Step 6 and slide 11 if different |
| T10 | [Step 6: citations](../docs/06-connect-and-ask-gridscribe.md) | Source URLs survive retrieval and private-source citations can be checked |
| T11 | [Step 8](../docs/08-optional-rag-in-code.md) | Cloud Shell end-to-end Entra/key tests, schema/vectorizer and failure paths |
| T12 | [Troubleshooting](../docs/troubleshooting.md) | Only if the Search tool fails to attach: try Foundry IQ once and time it for the backup demo |
| T13 | [Screenshot list](../docs/images/README.md) | Replace all five placeholders with real redacted captures and check image links |
| T14 | [Run sheet](run-sheet.md) | Novice timings, four-minute slides 3–7, current slide 13 credentials and approved slide 14 contacts |
| T15 | [Publication checks below](#publication-checks) | WSP approval, destination repo, links, help labels and social preview |

## Repository setup

- Create the GitHub repository **`wsp-gridscribe-lab`** in the approved owner/organisation after brand approval. This pack has been written locally; no remote repository or Azure resource was created by the authoring task.
- Description: **WSP GridScribe lab: build a standards-aware RAG assistant on Microsoft Azure**
- Topics: `azure`, `ai-search`, `ai-foundry`, `rag`, `workshop`, `energy`, `electrical-engineering`, `wsp`.
- Under **Settings** › **Social preview**, upload the supplied [social-preview.png](../assets/brand/banners/social-preview.png).
- Create issue labels **`help`** and **`lab`** so the [help template](../.github/ISSUE_TEMPLATE/i-am-stuck.md) works as intended.
- Preview Markdown in GitHub, including dark/light banners, Mermaid, collapsible answers and moving-logo footer. Markdown body fonts are platform-controlled.
- Test **Code** › **Download ZIP** from the actual student access level. Private-repo access must be arranged before the session; do not spend account-creation time granting GitHub permissions.
- The optional extension prompts for the real clone URL, so no fictitious owner or token is embedded in the code.
- The [MIT licence](../LICENSE) covers code/lab text only. Supplied WSP names/logos/brand assets are excluded.

### Publication checks

> [!NOTE]
> TODO (facilitator): verify in dry run — obtain WSP brand/marketing approval before making the repository public; confirm the destination owner, student download access, rendered pages, `help`/`lab` labels and social preview. Check any supplied copyright attribution with the appropriate owner before publication.

## Source decisions worth keeping

- [Blob indexer](https://learn.microsoft.com/azure/search/search-how-to-index-azure-blob-storage) supports **Markdown**: preserve the requested filenames rather than introduce unnecessary conversions.
- [Integrated vectorisation](https://learn.microsoft.com/azure/search/vector-search-integrated-vectorization) works on all tiers. The [portal vector quickstart](https://learn.microsoft.com/azure/search/search-get-started-portal-import-vectors) uses Basic only because it uses managed identity; its managed-identity checkbox is optional, so the lab uses keys on Free. The **Microsoft Foundry** embedding kind needs a managed identity, so Step 5 uses the **Azure OpenAI** kind with an API key.
- [Search limits](https://learn.microsoft.com/azure/search/search-limits-quotas-capacity): 36 sources fit document/file/storage limits; shared capacity and embedding quota still prevent a guaranteed one-run time. Do not confuse source size with vector/index size.
- [Semantic billing](https://learn.microsoft.com/azure/search/semantic-how-to-enable-disable) now has a free plan across pricing tiers. The primary path deliberately uses ordinary hybrid and no paid semantic billing.
- The [Azure AI Search tool](https://learn.microsoft.com/azure/foundry/agents/how-to/tools/ai-search) builds citations from the index's `title` and `url` fields, hence the added `url` field; [tool compatibility](https://learn.microsoft.com/azure/foundry/agents/concepts/limits-quotas-regions) covers the selected models. Direct integration avoids the extra Foundry IQ layer.
- [Retirement schedule](https://learn.microsoft.com/azure/foundry/openai/concepts/model-retirement-schedule) rules out recommending GPT-4.1-family models to fresh accounts. The old classic path's detailed screenshots are not evidence of equivalent new-portal controls.
- [Foundry IQ](https://learn.microsoft.com/azure/foundry/agents/concepts/what-is-foundry-iq) is the alternative to validate, not a second student build.
- The library contains question-only noise mentions in three project files **by explicit agreement**; there is no noise limit, acoustic criterion or guidance. Do not report a zero-mentions check as passed.

> [!WARNING]
> Record and verify cleanup for both the rehearsal and the live demonstration. A saved budget is useful but does not stop spend.

---
[← Previous](solution-walkthrough.md) · [Home](../README.md) · [Next →](run-sheet.md)

WSP AI Accelerator · UoC Insight Day 2026
