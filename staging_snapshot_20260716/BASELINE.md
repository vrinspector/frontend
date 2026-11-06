# Staging Baseline Snapshot — July 16, 2026 (Frontend)

Provenance record for the frontend artifacts deployed to staging and production as of the July 15, 2026 deployments. Source of truth: VR Inspector Transfer Package (Dropbox: `Projects_and_Engineering/VR_Inspector/VRInspector_Transfer_Package_20260716/03_Current_Implementation/`).

This repo had not been pushed since May 2026 while deployments went server-direct. The byte-exact HTML files are **pending commit** — they could not be transferred byte-exact through the automated channel available on 2026-11-06 (Dropbox text extraction strips HTML), so they are to be committed from a local copy of the Dropbox package and verified against the checksums below before merge.

| File (package name) | Deployed location | SHA-256 (documented, PRD v2.61) | Status |
|---|---|---|---|
| `staging_index_with_help_private.html` | `/opt/vrinspector/frontend/dist/index.html` (staging, current: Block 8E + mobile hotfix + authz + Help) | `915fe8d699a8bda68cdc179b9de7f62650fad677176777b3488a48faafef61bd` | Pending byte-exact commit |
| `staging_index_block8e.html` | staging frontend prior to Help overlay (authz-hardened) | `1fa33329f4cc90706b753c8285a2955c47a03c1cf8f24c3d468a46a114506757` | Pending byte-exact commit |
| `public_help_private_review.html` | `/opt/vrinspector/www/help/index.html` (production `/help/`) | `b8f36ef5bfb60537e643791977793f0c3c6002ae3376f2ef41df91b61bc54eb8` | Pending byte-exact commit |

Verification rule: before merging the HTML files into this snapshot, `sha256sum` each and confirm it matches the table above. If a checksum does not match, stop and reconcile against the Dropbox package and PRD v2.61.

These files are a historical record and the UI porting spec for the Phase 2 rebuild in `vrinspector/app` (REBUILD_PLAN.md increments 06–10). Do not edit them; rebuild work happens in `vrinspector/app`.
