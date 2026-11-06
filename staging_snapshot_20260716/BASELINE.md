# Staging Baseline Snapshot — July 16, 2026 (Frontend)

Byte-exact copies of the frontend artifacts deployed to staging and production as of the July 15, 2026 deployments, taken from the VR Inspector Transfer Package (Dropbox: `Projects_and_Engineering/VR_Inspector/VRInspector_Transfer_Package_20260716/03_Current_Implementation/`).

Purpose: this repo had not been pushed since May 2026 while deployments went server-direct. This snapshot makes Git match staging and serves as the UI porting spec for the Phase 2 rebuild in `vrinspector/app` (PRD v2.63 / REBUILD_PLAN.md increments 06–10).

| File | Deployed location | SHA-256 | Verified |
|---|---|---|---|
| `staging_index_with_help_private.html` | `/opt/vrinspector/frontend/dist/index.html` — current staging SPA (Block 8E + mobile hotfix + authz hardening + Help) | `915fe8d699a8bda68cdc179b9de7f62650fad677176777b3488a48faafef61bd` | Matches PRD v2.61 documented deployed checksum (verified 2026-11-06) |
| `staging_index_block8e.html` | staging SPA prior to the Help overlay (authz-hardened) | `1fa33329f4cc90706b753c8285a2955c47a03c1cf8f24c3d468a46a114506757` | Matches PRD v2.61 documented deployed checksum (verified 2026-11-06) |
| `public_help_private_review.html` | `/opt/vrinspector/www/help/index.html` — production `https://vrinspector.com/help/` | `b8f36ef5bfb60537e643791977793f0c3c6002ae3376f2ef41df91b61bc54eb8` | Matches PRD v2.61 documented deployed checksum (verified 2026-11-06) |

Notes:

- These files are a historical record. Do not edit them; rebuild work happens in `vrinspector/app`.
- The single-file SPA (`staging_index_with_help_private.html`) is the authoritative reference for screen behavior, pin-overlay math, and PDF.js viewer logic during the port.
- Rollback files and full deployment evidence: PRD v2.61 and the transfer package (`04_Evidence/`).
