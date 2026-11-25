# vex-scope-demo (TEST)

Test data for the repository/expiry scope filter proposed for `lidofinance/actions`
(`k8s-harbor-helper scope-vex`). Same layout and fields as `lidofinance/vex`.

| Statement | `whitelist_repositories` | `whitelist_expires` |
|---|---|---|
| GHSA-2xp9-vwfh-vxw4, GHSA-2464-fhr4-w9xw on `pkg:npm/next@12.3.7` | `myTestOrg0/ethereum-staking-widget-1` | 2027-01-23 (valid) |
| same | `myTestOrg0/staking-vault-widget` | 2026-11-01 (expired) |

Any other repository gets nothing from this source.
