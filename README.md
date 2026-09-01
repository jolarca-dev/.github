# .github — Organization-Wide Defaults

This repository contains shared configuration for all `jolarca-dev` organization repositories.

## What's Here

```
.github/
├── workflows/
│   ├── ci-base.yml          # Reusable CI baseline
│   ├── compliance-base.yml  # Shared compliance checks
│   └── security-scan.yml    # Unified security scanning
├── ISSUE_TEMPLATE/
│   └── config.yml           # Issue template chooser
├── PULL_REQUEST_TEMPLATE.md # Org-wide PR template
└── profile/
    └── README.md            # Organization profile page
```

## Reusable Workflows

### CI Base (`ci-base.yml`)

Provides consistent CI checks across all repos:
- Governance file presence validation
- Conventional Commits enforcement
- Secret scanning (gitleaks)
- YAML syntax validation
- Optional Python/JS/Terraform linting

**Usage in your repo:**

```yaml
# .github/workflows/ci.yml
name: CI
on:
  pull_request:
  push:
    branches: [main]

jobs:
  ci:
    uses: jolarca-dev/.github/.github/workflows/ci-base.yml@main
    with:
      run-python-lint: true
      run-terraform-fmt: true
```

### Compliance Base (`compliance-base.yml`)

Provides consistent compliance checks:
- Evidence integrity verification
- Policy review date monitoring
- Vendor assessment date tracking
- DSR SLA monitoring
- Retention schedule compliance

**Usage:**

```yaml
jobs:
  compliance:
    uses: jolarca-dev/.github/.github/workflows/compliance-base.yml@main
    with:
      check-evidence-integrity: true
      check-dsr-sla: true
```

### Security Scan (`security-scan.yml`)

Provides consistent security scanning:
- Dependency vulnerability scanning (Trivy)
- Container image scanning
- IaC scanning (Checkov)
- License compliance checking

**Usage:**

```yaml
jobs:
  security:
    uses: jolarca-dev/.github/.github/workflows/security-scan.yml@main
    with:
      scan-dependencies: true
      scan-iac: true
```

## Compliance

This repository supports:
- **SOC 2** CC8.1 (change management)
- **ISO 27001** A.8.25 (secure SDLC)
- **GDPR** Art. 25 (data protection by design)

## License

Internal use only. See [LICENSE](LICENSE).
