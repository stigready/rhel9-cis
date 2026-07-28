# Changelog

Format based on [Keep a Changelog](https://keepachangelog.com/).

## [0.2.1-private-review] - export review

### Added
- Initial StigForge export of matrix role `rhel9_cis`.
- OpenSCAP verify evidence bundles per profile under `compliance/releases/`.

### Verified (CI)

- **`cis-l1`** — score **97.33%** (floor 90.0%) · gate **PASS** · evidence `20260726T140136Z`
  - OpenSCAP failures still counted: `configure_custom_crypto_policy_cis, file_permissions_ungroupowned`
- **`cis-l2`** — score **97.4%** (floor 90.0%) · gate **PASS** · evidence `20260726T140502Z`
  - OpenSCAP failures still counted: `configure_custom_crypto_policy_cis, file_permissions_ungroupowned`

### Provenance

- Factory pipeline: https://github.com/stigready/stigforge/actions/runs/30277229616
- Factory commit: `ccc5f55bd24b1c9cb1b8ca95a70b55443e0064b5`

