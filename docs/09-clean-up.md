<img src="../assets/brand/logo/wsp-logo-red.png" alt="WSP" height="28">

[Home](../README.md) › Step 9

# Step 9 — Protect your free credit

**Allow 2–3 minutes to start deletion, then verify completion.**

> [!WARNING]
> Do this before leaving, even if the build failed. **Basic Search bills while idle.** Closing the browser does not stop a resource. Deleting the group permanently deletes its contents, so check the name carefully and save any draft/checklist you want first.

## 1. Delete the workshop group

1. In [Azure portal](https://portal.azure.com), open **Resource groups** › **`rg-gridscribe-<initials>`**.
2. Check the subscription and resources. They should be **your** storage account, Search service and Foundry parent/project, plus any lab-created dependencies.
3. Select **Delete resource group**, type the exact group name and confirm **Delete**.
4. Wait for the notification. Refresh Resource groups until that group is gone. If deletion fails, open the error and ask the facilitator; do not assume the click succeeded.

## 2. Check for strays

In **All resources**, filter to your workshop subscription and inspect names created today. Look especially for a second Basic Search service, a Foundry resource accidentally put in another group, and optional Cloud Shell storage. Delete **only your lab resources**; never remove a shared or unrelated resource. Model deployments disappear with their Foundry parent.

If Cloud Shell created a separate storage account, remove its lab-only file share/account only when you are sure it contains nothing else you need. Ephemeral Cloud Shell avoids this extra storage. Do not delete a group just because its name looks unfamiliar.

## 3. Set a budget alert

Open **Cost Management + Billing** › **Cost Management** › **Budgets** (at subscription scope) › **Add**. Use name `gridscribe-safety`, monthly amount **5 in the subscription's billing currency**, alerts at **50%, 80% and 100% actual cost**, and your own email as the recipient. Choose the current period and review the dates shown. Check **Cost analysis** and remaining credit later; reporting is delayed.

> [!IMPORTANT]
> A budget is an **alert, not a spending cap**, and does not reserve free credit or shut resources down. Some offer types restrict budget creation; if the control is unavailable, check credit/Cost analysis and verify deletion instead. Do not upgrade just to add an alert.

**Expected result:** the workshop group no longer exists, no stray lab resources remain, and a budget is saved if your offer supports it.

**If it fails:** read deletion/permission errors, remove only lab-specific locks if you deliberately set them, and tell the facilitator. Keep checking until deletion completes.

Official guidance: [delete resource groups](https://learn.microsoft.com/azure/azure-resource-manager/management/delete-resource-group), [create budgets](https://learn.microsoft.com/azure/cost-management-billing/costs/tutorial-acm-create-budgets).

---
[← Previous](08-optional-rag-in-code.md) · [Home](../README.md) · [Next →](../README.md)

WSP AI Accelerator · UoC Insight Day 2026
