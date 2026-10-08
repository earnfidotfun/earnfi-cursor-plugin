---
name: fund-marketplace-order
description: Create and fund an EarnFi marketplace order (escrow).
---

Load **marketplace-order** skill. Sequence `earnfi_order_create` → `earnfi_order_fund` with pay-first signatures. Confirm order id and next deliver/release steps.
