# vex-scope-demo (TEST)

Test data for the repository/expiry scope filter proposed for `lidofinance/actions`
(`k8s-harbor-helper scope-vex`). Same layout and fields as `lidofinance/vex`.

| Repository | GHSA-2xp9-vwfh-vxw4 | GHSA-2464-fhr4-w9xw |
|---|---|---|
| `myTestOrg0/ethereum-staking-widget-1` | until 2027-01-23 (valid) | until 2026-11-01 (expired) |
| `myTestOrg0/staking-vault-widget` | until 2026-11-01 (expired) | until 2027-01-23 (valid) |

Any other repository gets nothing from this source.

## Data for the options A–E test (`options/`)

| Option | Data | myTestOrg0/ethereum-staking-widget-1 | myTestOrg0/staking-vault-widget |
|---|---|---|---|
| A. global VEX | `options/a-global/` (plain package statements, no custom fields) | both GHSAs | both GHSAs |
| B. image statements | `options/b-oci/` (image `team-si/staking-widget` + `next@12.3.7` as subcomponent) | both (image name `staking-widget`) | none (image name `staking-vault-widget`) |
| C. scope-vex filter | `pkg/npm/next/vex.json` + `whitelist_*` fields | GHSA-2xp9 only (GHSA-2464 expired) | GHSA-2464 only (GHSA-2xp9 expired) |
| D. central per-repo VEX | `options/d-vex/repos/<owner>/<repo>/vex.json` | both | none (no file) |
| E. central per-repo .trivyignore.yaml | `options/e-trivyignore/repos/<owner>/<repo>.trivyignore.yaml` | GHSA-2xp9 only (GHSA-2464 `expired_at` 2026-11-01) | none (no file) |
