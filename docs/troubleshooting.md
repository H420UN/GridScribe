<img src="../assets/brand/logo/wsp-logo-red.png" alt="WSP" height="28">

[Home](../README.md) › Troubleshooting

# Stuck? Start here

**Two-minute rule:** if the next fix is not quick, pair up or ask Haroun to demonstrate from the prepared environment. Keep the engineering/evidence exercise going.

## Account and browser

| What you see | Try this |
| --- | --- |
| Card declined, prepaid or virtual card | Use an eligible debit/credit card if comfortable, Azure for Students if eligible, or pair up. Do not share cards or remove spending protection. |
| No verification text | Check country code and number; wait before resending. Ask for help rather than repeatedly registering. |
| Verification page hangs | Allow required third-party cookies for sign-up, disable blocking extensions temporarily for that page, or try another browser. |
| University email not accepted | Check full-time/18+ eligibility; switch to Azure free account if eligible, or pair up. |
| "Free account already used" | The offer is limited to eligible new customers. Use an existing suitable subscription only with cost awareness, or pair up. Do not create identities to evade offer restrictions. |
| Wrong directory / no subscription | Match account, directory and subscription in both portals. Check **Subscriptions** says **Active**. |
| Pop-up blocked | Allow pop-ups for Azure/Foundry only; retry the sign-in or model picker. |
| Student cannot deploy model | Allowed-region policy and model quota are separate. Check **Manage** › **Quota** › **Show all**. Try an allowed approved region, Azure free account if eligible, or pair up. A free trial may also have no quota. |

## Resources and indexing

| What you see | Try this |
| --- | --- |
| Storage name taken | Change four digits; lowercase letters/numbers only, no hyphens in storage account names. |
| Free Search unavailable | One Free service per subscription. Do not delete an existing unrelated service. With facilitator agreement, create **Basic**, check the displayed price and delete straight after the session. Free cannot simply be scaled up. |
| Wizard requires a managed identity | Untick **Authenticate using managed identity** and choose **API key** for the embedding model (Step 5). If the portal still insists, pair up, or use the facilitator-approved Basic fallback in [Step 3](03-create-ai-search.md). |
| Region does not support chosen path | Verify Search, models and agent tool in that region, as well as policy and quota. Agree a fallback before creating more resources. |
| Embedding deployment missing | Check same account/tenant/subscription, Foundry project provider, parent resource and deployment **Succeeded**. The deployment name is `text-embedding-3-small`; chat is not an embedding deployment. Allow refresh time. |
| 401/403 in wizard | Confirm storage/model keys are permitted, or use the correct Search identity and target-resource RBAC roles from [Step 5](05-index-the-library.md). Your own user and service identities are not interchangeable. |
| Indexer processes 0 documents | Verify container `library`, no subfolder filter, 36 actual blobs not a ZIP, and no extension exclusion. Markdown is supported; if the portal rejects a particular file, read its failure detail instead of assuming all `.md` files are unsupported. |
| Indexer stops part-way | Inspect execution details and [Free limits](03-create-ai-search.md). For timeout/429, wait at least 180 seconds and **Run** again, not Reset. A daily enrichment allowance is not fixed by rerunning. Skip OCR/language enrichment; embeddings have their own billing and quota. |
| 36 index documents, but missing sources | The count is chunks, not files. Check execution history and source names. Duplicate uploads can inflate it. |
| `url` absent or empty | You skipped the **Add field** step in [Step 5](05-index-the-library.md). Delete the index, indexer, data source and skillset, then rerun the wizard and add `url` (source `metadata_storage_path`, Retrievable). |
| Vector query fails | Compare `text_vector` dimensions and its vector profile/vectorizer with the embedding deployment. Read the actual schema, not guessed field names. |

## Answers and citations

| What you see | Try this |
| --- | --- |
| Fluent answer with no citations | Check Search tool actually ran, instructions saved, content/source fields retrievable and source URL populated. Start a fresh conversation. |
| Citation marker points nowhere | Inspect source URL mapping. Private Blob links may require opening the source through authenticated Storage or the downloaded library. **Do not enable anonymous access.** |
| Cites a superseded edition | Inspect retrieved chunks for current status and date; retrieve the current edition/amendment explicitly. Tighten the edition rules, save, then retest the same question. Stronger instructions cannot quote an absent chunk. |
| Draft treated as a requirement | Reinforce the draft/advisory rule. Check current EESB-305:2022 was retrieved, not just the 2026 proposal. |
| Noise question gets an invented number | A project question is not evidence for a limit. Require **No source found in the library**, inspect retrieval, remove outside knowledge tools and rerun the pressure test. |
| Default semantic query fails | Select `vector_simple_hybrid` for the primary path. Semantic configurations and free billing allowances are separate; do not enable paid ranking to hide a configuration error. |
| Model unavailable / 429 | Check per-model, per-region quota, deployment type and current lifecycle. Use only the approved fallback models or regions, or pair/demo. Catalogue visibility is not deployability. |

## If you cannot attach the Search tool to the agent

In the session, **pair up** with someone whose agent works, or watch the facilitator's prepared GridScribe: the evidence exercise in [Step 7](07-test-and-evaluate.md) matters more than the clicks. Do not swap to a classic agent or an older model to get round it.

Two other ways to ground a chat model in `gridscribe-index`, to try after the session:

- **Foundry IQ knowledge base.** New Foundry › **Build** › **Knowledge**: connect your Search service, add a **search-index knowledge source** pointing at the existing `gridscribe-index` (not a Blob source, which would build a second index), create a knowledge base, then connect it to an agent. It adds query planning, which can add small extra charges. See [What is Foundry IQ?](https://learn.microsoft.com/azure/foundry/agents/concepts/what-is-foundry-iq), [existing-index knowledge source](https://learn.microsoft.com/azure/search/agentic-knowledge-source-how-to-search-index) and [connect to an agent](https://learn.microsoft.com/azure/foundry/agents/how-to/foundry-iq-connect).
- **Chat playground "Add your data".** Where the playground still offers it for your model, select Azure AI Search › `gridscribe-index`, hybrid search. It is an older route and may not be offered for newer models.


- **Storage prompt:** choose ephemeral / no storage if available. If persistence is required, use advanced settings and create any storage in the workshop group, or record the separate lab-only storage for deletion. Do not delete an existing Cloud Shell share belonging to other work.
- **Permissions:** the script's user needs Search Index Data Reader and Cognitive Services OpenAI User. The index vectorizer independently needs access to its embedding model.
- **No answer / non-zero exit:** read the diagnostic. Empty retrieval is explicitly reported; permission and service errors are not disguised as "No source found".
- **Partial response:** a token limit or content filter is not a successful answer; rerun with a shorter question or review the deployment.

> [!WARNING]
> Never put a key, connection string, token, phone number, card detail or real client content into a help issue. Use the [help template](../.github/ISSUE_TEMPLATE/i-am-stuck.md) with redacted errors only. [Clean up](09-clean-up.md) even after a failed build.

---
[← Previous](09-clean-up.md) · [Home](../README.md) · [Next →](../facilitator/backup-plan.md)

WSP AI Accelerator · UoC Insight Day 2026
