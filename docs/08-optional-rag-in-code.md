<img src="../assets/brand/logo/wsp-logo-red.png" alt="WSP" height="28">

[Home](../README.md) › Step 8

# Step 8 — Optional: see RAG in code

**Allow another 10–15 minutes after the workshop.** The main lab needs no terminal. This extension runs in **Azure Cloud Shell (Bash)** in your browser: no local installs.

The [script](../scripts/ask_gridscribe.py) is roughly 130 lines including validation and errors. It exposes the same pattern as the portal, but **does not invoke the saved agent**: it loads the same instructions, retrieves five chunks with hybrid search, and calls your chat deployment directly. Outputs can differ from the agent's multi-step retrieval.

## 1. Open Cloud Shell and clone

1. In [Azure portal](https://portal.azure.com), select the **Cloud Shell** terminal icon, then **Bash**.
2. Choose **No storage account required** / an ephemeral session if offered. Otherwise use the workshop subscription, **advanced storage settings** and `rg-gridscribe-<initials>` for any new storage. Do not let a default create an untracked group. Cloud Shell storage may cost money; see [troubleshooting](troubleshooting.md).
3. On the repository's GitHub page, **Code** › **HTTPS** › copy the clone URL. Paste it at the prompt below; this avoids inventing an organisation/repository URL:

```bash
read -r -p "Paste this repository's HTTPS clone URL: " LAB_REPO_URL
git clone "$LAB_REPO_URL" wsp-gridscribe-lab
cd wsp-gridscribe-lab
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r scripts/requirements.txt
```

For a private repository, authenticate with GitHub's supported flow, not a token embedded in the clone URL. Python 3.10+ is required. Versions are pinned in [requirements](../scripts/requirements.txt), checked against PyPI on 13 November 2026.

## 2. Grant your signed-in user access

Cloud Shell is already signed in to Azure. `DefaultAzureCredential` uses that Azure CLI identity; do not paste a password or access token.

In Azure portal › each target resource › **Access control (IAM)** › **Add role assignment**:

| Resource | Assignee | Role |
| --- | --- | --- |
| Search service | Your personal Azure user | **Search Index Data Reader** |
| Foundry parent resource | Your personal Azure user | **Cognitive Services OpenAI User** for its Azure OpenAI model endpoint |

Also enable Search role-based API access under **Settings** › **Keys** › **Both** or **Role-based access control**. A subscription Owner role does not automatically grant model/data-plane access. Roles can take several minutes to propagate.

The **Search index vectorizer** must itself be authorised to call the embedding model: it uses the key/managed identity configured in Step 5, **not automatically your Cloud Shell identity**. The script sends `VectorizableTextQuery`; the index embeds the question using its configured vectorizer. It does not need a separate embedding-model environment variable.

## 3. Set non-secret environment values

```bash
cp scripts/.env.example .env
nano .env
# Replace every <placeholder>; save with Ctrl+O, Enter, then Ctrl+X.
source .env
```

Use the **Azure OpenAI resource endpoint** shown by the parent Foundry resource's **Keys and Endpoint** / model code sample, such as `https://your-resource.openai.azure.com`. Do not use the project `/api/projects/...` endpoint or paste `/openai/v1/`; the script adds that API path.

| Variable | Value |
| --- | --- |
| `AUTH_MODE` | `entra` (default) |
| `AZURE_SEARCH_ENDPOINT` | Search Overview HTTPS endpoint |
| `AZURE_SEARCH_INDEX` | `gridscribe-index` |
| `AZURE_OPENAI_ENDPOINT` | Foundry parent model endpoint, no path |
| `AZURE_OPENAI_CHAT_DEPLOYMENT` | `gridscribe-chat`, not `<CHAT_MODEL>` or the catalogue label |
| `SEARCH_CONTENT_FIELD` / `SEARCH_TITLE_FIELD` | `chunk` / `title` |
| `SEARCH_SOURCE_FIELD` / `SEARCH_VECTOR_FIELD` | `url` / `text_vector` |

Inspect the index's **Fields** and vector profile if your wizard uses different names. `url` must be retrievable and populated from the Blob path (you added it in Step 5).

## 4. Ask and expose retrieval

```bash
python scripts/ask_gridscribe.py "What is the minimum BESS spacing?" --show-chunks
python scripts/ask_gridscribe.py "What is the inverter noise limit?"
```

`--show-chunks` prints the actual numbered passages and source metadata. The answer is followed by **Sources**, listing retrieved candidates, not a guarantee of valid citations. Open the originals and evaluate as in [Step 7](07-test-and-evaluate.md).

## Explicit API-key fallback

Use only if Entra access is blocked and the facilitator agrees. Search › **Keys** › **Manage query keys** provides a **query key** (not an admin key); Foundry parent › **Keys and Endpoint** provides the model key. Both resources must permit API-key access.

```bash
export AUTH_MODE=key
read -r -s -p "Search query key (hidden): " AZURE_SEARCH_API_KEY; printf '\n'
export AZURE_SEARCH_API_KEY
read -r -s -p "Foundry model key (hidden): " AZURE_OPENAI_API_KEY; printf '\n'
export AZURE_OPENAI_API_KEY
python scripts/ask_gridscribe.py "What is the minimum BESS spacing?" --show-chunks
unset AZURE_SEARCH_API_KEY AZURE_OPENAI_API_KEY
```

> [!WARNING]
> Never print keys, enable `set -x`, put keys in a command-line argument, commit `.env`, or share terminal screenshots containing secrets. A query key cannot change an index. Delete or rotate exposed keys immediately.

**Expected result:** five or fewer labelled chunks, a grounded draft answer and a Sources list; an empty retrieval gives **No source found in the library** without a generation call. Failures exit non-zero with a diagnostic; API response bodies are not printed.

**If it fails:** 401/403 → roles, sign-in or API-access setting; 429 → model quota; unknown field/vectorizer error → check actual index schema and Step 5 configuration. Never suppress errors and present an empty answer as success.

Offline checks (no Azure requests): `python -m unittest discover -s scripts -p 'test_*.py'`.

> [!NOTE]
> TODO (facilitator): verify in dry run — run the optional script in Cloud Shell with Entra roles, then its explicit key fallback, using the actual wizard-created schema and vectorizer. Confirm citations and both empty-retrieval and permission-failure behaviour end to end.

SDK sources: [hybrid queries](https://learn.microsoft.com/azure/search/hybrid-search-how-to-query), [query vectorisation](https://learn.microsoft.com/azure/search/vector-search-how-to-configure-vectorizer), [OpenAI endpoint authentication](https://learn.microsoft.com/azure/developer/ai/how-to/switching-endpoints?pivots=python).

---
[← Previous](07-test-and-evaluate.md) · [Home](../README.md) · [Next →](09-clean-up.md)

WSP AI Accelerator · UoC Insight Day 2026
