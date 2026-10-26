# ACP Legacy Extractor

Extracts data from a legacy dealer management system and writes it in the
source-agnostic ACP migration CSV format, so it can be loaded through the ACP
legacy import (dry-run, then apply).

This repo lives outside the main ACP platform on purpose: the extraction is
specific to the legacy system, while ACP only knows the generic import contract.

## Rules

- Public repo: never commit customer data, exports, credentials, connection
  strings or real customer/company names. Use synthetic fixtures only.
- Do not copy proprietary source definitions, schemas or code excerpts from the
  legacy system. Map only to the ACP migration CSV format.
- Output must match the ACP migration CSV specs (customers, vehicles, history,
  open orders, tyres) in the `auto-core-platform` repo.
