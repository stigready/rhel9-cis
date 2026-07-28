# stigready/rhel9-cis

StigForge-exported Ansible role **`rhel9_cis`** · release **`0.2.1-private-review`**.
Matrix cell status: **`green`**.

## Install (Ansible Galaxy)

This repository root **is** the Ansible role (Galaxy-style layout). OpenSCAP evidence
lives under `compliance/` and is not loaded when the role runs.

```yaml
# requirements.yml
roles:
  - src: https://github.com/stigready/rhel9-cis
    scm: git
    version: v0.2.1-private-review   # or an immutable commit SHA
    name: rhel9_cis
```

```bash
ansible-galaxy role install -r requirements.yml -p ./roles
ansible-playbook -i inventory site.yml   # role: rhel9_cis
```

## Verification status (this release)

Evidence was produced by **docker verify + OpenSCAP** on the factory CI run cited below.

| Profile | Score | Floor | Gate | Ansible | Evidence tested (UTC) |
|---|---:|---:|---|---|---|
| `cis-l1` | **97.33%** ✓ | 90.0% | PASS ✓ | rc 0 | 20260726T140136Z |
| `cis-l2` | **97.4%** ✓ | 90.0% | PASS ✓ | rc 0 | 20260726T140502Z |

Full artifacts per profile: `compliance/releases/0.2.1-private-review/<profile>/` (`score.json`, `results.xml`, `report.html`, `evidence.json`, `evidence-report.html`, `poam.md`).

## Reports & review

- **[REVIEW.md](REVIEW.md)** — linked evidence index for product owner review
- **[reports/index.html](reports/index.html)** — HTML report index
- **[CHANGELOG.md](CHANGELOG.md)** — release notes and verify summary

## License

- **[LICENSE](LICENSE)** (MIT) — StigForge export packaging
- **[NOTICE](NOTICE)** — ComplianceAsCode / BSD-3-Clause task body attribution

## Factory

- Monorepo: [stigready/stigforge](https://github.com/stigready/stigforge) @ `ccc5f55bd24b1c9cb1b8ca95a70b55443e0064b5`
- CI run: https://github.com/stigready/stigforge/actions/runs/30277229616
- Catalog: [https://stigready.com/#stigforge](https://stigready.com/#stigforge)

