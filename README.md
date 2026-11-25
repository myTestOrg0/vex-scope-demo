# vex-scope-demo (TEST)

Test data for the repository/expiry scope filter proposed for `lidofinance/actions`
(`k8s-harbor-helper scope-vex`). Same layout and fields as `lidofinance/vex`.

| Repository | GHSA-2xp9-vwfh-vxw4 | GHSA-2464-fhr4-w9xw |
|---|---|---|
| `myTestOrg0/ethereum-staking-widget-1` | until 2027-01-23 (valid) | until 2026-11-01 (expired) |
| `myTestOrg0/staking-vault-widget` | until 2026-11-01 (expired) | until 2027-01-23 (valid) |

Any other repository gets nothing from this source.
