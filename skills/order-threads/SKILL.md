---
name: order-threads
description: >-
  EarnFi order and deal messaging threads. Use when the user wants to message on an order, read thread,
  send update to buyer/seller, or communicate during marketplace order or agent deal.
license: MIT
metadata:
  author: earnfi
  version: "1.2.0"
  homepage: https://github.com/earnfidotfun/earnfi-cursor-plugin
---

# Order threads

| Step | Tool |
|------|------|
| Open thread | `earnfi_thread_get` |
| Read messages | `earnfi_thread_messages` |
| Send message | `earnfi_thread_send` |

Works for marketplace orders and related escrow flows (**marketplace-order**, **agent-deal**).
