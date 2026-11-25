<img src="../assets/brand/logo/wsp-logo-red.png" alt="WSP" height="28">

[Home](../README.md) › Step 4

# Step 4 — Foundry and the two models

**4 minutes target, including deployment.** Your account's quota decides what is possible; a model card appearing in the catalogue does not guarantee a deployment.

## 1. Check before creating

Use **Sweden Central** first; fallbacks are **East US 2**, then **UK South**. These support Foundry projects and Agent Service in current documentation, but you must also check [model availability](https://learn.microsoft.com/azure/foundry/foundry-models/concepts/models-sold-directly-by-azure-region-availability), quota and your subscription's allowed locations.

## 2. Create one Foundry resource and project

1. Sign in to [ai.azure.com](https://ai.azure.com) with the same account as Azure portal. Turn **New Foundry** on for these creation steps.
2. In the project dropdown select **Create a new project**. Name it `gridscribe-<initials>`.
3. Expand **Advanced options**. Select the **existing** subscription and `rg-gridscribe-<initials>`, and the agreed region. If offered a resource name, use `ai-gridscribe-<initials>-<4 digits>`. Otherwise record the generated parent resource name; do not create a second resource simply to rename it.
4. Select **Create project**. Verify the parent resource is in your workshop resource group, with public networking for this fictional-only lab. Avoid hub-based projects, managed compute and provisioned deployments.

## 3. Deploy the chat model

1. In New Foundry go to **Build** › **Catalog** › **Model Catalog**.
2. Find **gpt-5.4-mini**; if quota/tool support is unavailable, use the dry-run-approved fallback.
3. Select **Deploy** › **Custom settings**. Deployment name **`gridscribe-chat`**, deployment type **Global Standard** if available, smallest offered non-zero capacity adequate for one pair. Do not use Batch or Provisioned.
4. Check the price and subscription, then **Deploy**. Under **Build** › **Models**, confirm **Succeeded**.

## 4. Deploy the embedding model

Repeat with **text-embedding-3-small**, deployment name **`text-embedding-3-small`**, **Standard** if available (or the dry-run-approved non-provisioned type), smallest adequate capacity. Keep its default **1,536 dimensions**. It converts passages to vectors; it does not answer questions.

> [!IMPORTANT]
> Both deployments consume credit when used. Global deployments can process requests outside the resource region. Use only the invented training documents; never real client information.


## 5. Keep the new portal selected

The primary path in [Step 6](06-connect-and-ask-gridscribe.md) uses a **new Foundry prompt agent** and the **Azure AI Search tool**. Leave **New Foundry on**. The [tool compatibility table](https://learn.microsoft.com/azure/foundry/agents/concepts/limits-quotas-regions#tool-support-by-region-and-model) lists Azure AI Search support for all three candidate models.

The [retirement schedule](https://learn.microsoft.com/azure/foundry/openai/concepts/model-retirement-schedule) currently lists these candidates as GA, but GPT-4.1-family models as deprecated and unavailable to new customers. Classic agents are also deprecated. Neither is a suitable fallback for a fresh account. Small `gpt-5-mini` is not a drop-in replacement either: its current tool matrix does **not** list direct Azure AI Search support.

**Expected result:** the correct project and resource group, plus two **Succeeded** deployments named `gridscribe-chat` and `text-embedding-3-small`.

**If it fails:** check **Manage** › **Quota** in New Foundry (Show all), model, region and remaining capacity; try only approved alternatives or pair up. Do not confuse the model's catalogue name with its deployment name.

Sources checked 13 November 2026: [resource/project quickstart](https://learn.microsoft.com/azure/foundry/tutorials/quickstart-create-foundry-resources), [model deployment](https://learn.microsoft.com/azure/foundry/foundry-models/how-to/deploy-foundry-models), [region support](https://learn.microsoft.com/azure/foundry/reference/region-support), [agent regions/models](https://learn.microsoft.com/azure/foundry/agents/concepts/limits-quotas-regions), [Azure AI Search tool](https://learn.microsoft.com/azure/foundry/agents/how-to/tools/ai-search).

---
[← Previous](03-create-ai-search.md) · [Home](../README.md) · [Next →](05-index-the-library.md)

WSP AI Accelerator · UoC Insight Day 2026
