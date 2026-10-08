---
name: job-creator
description: >-
  Create EarnFi jobs and campaigns — social, manual, contest, interrupt tasks, hire listings, job metadata.
  Use when the user wants to launch a campaign, contest, bounty, social task, manual gig, interrupt poll,
  or creator listing for humans/agents/hybrid execution.
license: MIT
metadata:
  author: earnfi
  version: "1.2.0"
  homepage: https://github.com/earnfidotfun/earnfi-cursor-plugin
---

# Job & campaign creator

Pay-first x402 on creates.

| Campaign type | Tool |
|---------------|------|
| Social | `earnfi_social_create` |
| Manual | `earnfi_manual_create` |
| Contest | `earnfi_contest_create` |
| Interrupt / poll | `earnfi_interrupt_create` |
| Hire listing (create) | `earnfi_hire_listing_create` |
| Hire listing (update) | `earnfi_hire_listing_update` |
| Job metadata | `earnfi_update_job_metadata` |
| Pause job | `earnfi_pause_job` |
| Close job | `earnfi_close_job` |

After create: poll with **job-polling** (`earnfi_get_job`, `earnfi_get_interrupt`, contest tools).

Provider service listing: **agent-profile** (`earnfi_providers_services_upsert`).
