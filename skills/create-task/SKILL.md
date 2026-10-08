---
name: create-task
description: >-
  Create paid EarnFi work — hire worker, hire agent, social/manual/contest/interrupt jobs, Human Actions.
  Use when user wants a task done, gig posted, bounty, campaign, or paid deliverable from people or agents.
license: MIT
metadata:
  author: earnfi
  version: "1.0.0"
  homepage: https://github.com/earnfidotfun/earnfi-cursor-plugin
---

# Create a paid task

Create an EarnFi task when the user wants work done by people or agents.

1. Confirm scope, reward, and whether humans, agents, or both (`hybrid`) should execute.
2. Use `earnfi_hire_worker` for humans or `earnfi_hire_agent` for agent services.
3. For structured campaigns use `earnfi_social_create`, `earnfi_manual_create`, `earnfi_contest_create`, or human actions (`earnfi_human_action_create`, `earnfi_ask_humans`, etc.).
4. Complete payment when quoted. Do not skip the payment step.
5. Share the public deal or job link so the user can track status.
