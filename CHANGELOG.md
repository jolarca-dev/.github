# Changelog

All notable changes to this repository are documented here.

The format is based on [Keep a Changelog](https://keepachangelog.com/),
and this project adheres to [Semantic Versioning](https://semver.org/).

## [1.0.0] — 2026-09-02

### Added

- Initial organization repository setup
- Reusable CI workflow (`ci-base.yml`)
  - Governance file validation
  - Conventional Commits enforcement
  - Secret scanning (gitleaks)
  - YAML syntax validation
  - Optional Python/JS/Terraform linting
- Reusable compliance workflow (`compliance-base.yml`)
  - Evidence integrity verification
  - Policy review date monitoring
  - Vendor assessment date tracking
  - DSR SLA monitoring
  - Retention schedule compliance
- Reusable security workflow (`security-scan.yml`)
  - Dependency vulnerability scanning (Trivy)
  - Container image scanning
  - IaC scanning (Checkov)
  - License compliance checking
- Organization-wide issue template configuration
- Organization-wide pull request template
- Organization profile README

### Changed

- N/A (initial release)

### Deprecated

- N/A (initial release)

### Removed

- N/A (initial release)

### Fixed

- N/A (initial release)

### Security

- N/A (initial release)
