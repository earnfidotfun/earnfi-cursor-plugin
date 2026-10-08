---
name: work-receipt
description: >-
  Work Receipt V1 — fetch and verify cryptographic proof of completed EarnFi work. Use for audit trail, proof of delivery, receipt ID lookup.
license: MIT
metadata:
  author: earnfi
  version: "1.0.0"
  homepage: https://github.com/earnfidotfun/earnfi-cursor-plugin
---

# Work Receipt V1

Every completed hire on EarnFi returns the same **Work Receipt V1** — human actions, agent orders, deals, job contracts, and open work.

## When work is done

Completion responses and webhooks include `work_receipt` automatically. You do not need to stitch payment proof and deliverables from separate calls.

## Lookup (pick one)

1. **By receipt id** — `earnfi_get_receipt` (verify semantics) or `earnfi_receipt_get` (raw fetch)
2. **By work reference** — `earnfi_get_work_receipt`

### ref_type examples

| Work type | ref_type | ref_id |
|-----------|----------|--------|
| Agent marketplace order | `agent_order` | order `public_slug` |
| Agent escrow deal | `agent_deal` | deal slug |
| Human custom deal | `deal` | deal slug |
| Human Action (ask/review/vote…) | `human_action` | `action_id` |
| Job contract | `job_contract` | contract slug |
| Job milestone | `job_milestone` | `{slug}:m{milestone_id}` |
| Open work acceptance | `open_work_submission` | `submission_id` |

## SDK

```ts
const { json } = await client.receipts.getWorkReceipt('human_action', actionId);
const receipt = json.work_receipt;

await client.receipts.verify(receipt.receipt_id);
```

## What is inside

- **work** — spec, acceptance mode, evidence
- **payment** — amount, fees, settlement_id, tx_hash
- **parties** — payer, payee, worker
- **links** — self, verify, lookup
- **verified** — on verify endpoint only

Show the user the receipt id and verify link when work completes. Keep copy short.
