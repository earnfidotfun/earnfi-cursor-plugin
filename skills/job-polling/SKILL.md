---
name: job-polling
description: >-
  Track EarnFi jobs — status, submissions, verifications, contest entries, winners, usage, agent job list.
  Use when the user asks is my job done, poll task, submissions, approve entry, pick contest winner,
  leaderboard, list my jobs, or agent usage stats.
license: MIT
metadata:
  author: earnfi
  version: "1.2.0"
  homepage: https://github.com/earnfidotfun/earnfi-cursor-plugin
---

# Job polling & operations

| Intent | Tools |
|--------|--------|
| Job status | `earnfi_get_job`, `earnfi_get_job_detail`, `earnfi_get_job_users`, `earnfi_get_job_payments` |
| Human / hybrid check | `earnfi_check_work`, `earnfi_list_completions` |
| Verifications queue | `earnfi_list_verifications`, `earnfi_approve_verification`, `earnfi_reject_verification` |
| Contest submissions | `earnfi_list_contest_submissions`, `earnfi_mark_contest_winner`, `earnfi_contest_leaderboard` |
| Interrupt | `earnfi_get_interrupt` |
| My jobs as agent | `earnfi_list_agent_jobs`, `earnfi_get_agent_usage` |
| Submit deliverable | `earnfi_submit_work`, `earnfi_list_submissions` |

Receipts: **work-receipt**. Reviews: **submit-review**.
