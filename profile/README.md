# Journey of Life — Marketplace Platform

**Building the most compliant marketplace in the Baltics.**

---

## 🏗️ Architecture

We operate a **90/10 hybrid infrastructure** topology:

- **90% Bare Metal** — Hardened PostgreSQL, Vault, MinIO, WireGuard mesh (Ansible-managed)
- **10% GCP** — GKE, Cloud DNS, IAM (Terraform-managed)
- **Zero Trust** — No public IPs, CMEK encryption everywhere, two-person rule for production changes

## 📦 Repository Fleet

| Repository | Purpose | Visibility |
|------------|---------|------------|
| [`jolarca`](https://github.com/jolarca-dev/jolarca) | Platform application (Django + Next.js) | Public |
| [`jolarca-infrastructure`](https://github.com/jolarca-dev/jolarca-infrastructure) | IaC: Terraform, Ansible, K8s, WireGuard | Public |
| [`jolarca-compliance`](https://github.com/jolarca-dev/jolarca-compliance) | SOC 2 / ISO 27001 / GDPR evidence | Private |
| [`jolarca-legal`](https://github.com/jolarca-dev/jolarca-legal) | Contracts, ToS, VAT OSS filings | Public |
| [`jolarca-data`](https://github.com/jolarca-dev/jolarca-data) | Analytics, retention-as-code, schemas | Private |

## 🛡️ Compliance Posture

We take compliance seriously — it's not an afterthought, it's architecture.

| Standard | Status | Anchor |
|----------|--------|--------|
| **SOC 2 Type II** | 🟢 Aligned | CC6.1, CC7.2, CC8.1 |
| **ISO 27001:2022** | 🟢 Aligned | A.5-A.18 controls |
| **GDPR** | 🟢 Compliant | Art. 5, 17, 25, 30, 32 |
| **PCI-DSS** | 🟢 SAQ-A | Stripe-hosted payments |

**Key principles:**

- **Retention as code** — Policy is executable, not prose
- **Evidence integrity** — Every audit artifact is hashed and manifest-tracked
- **Payment boundary** — PCI scope isolated from marketplace logic
- **Data residency** — EU-only processing, no transfers without TIA

## 🌍 Markets

**Pilot:** Lithuania 🇱🇹  
**Expansion:** Latvia 🇱🇻, Estonia 🇪🇪 (Q1 2027)  
**Target:** EU-27 by 2028

## 🔒 Security

- **Bug bounty:** Coming soon
- **Vulnerability disclosure:** See `SECURITY.md` in each repository
- **Security contacts:** security@jolarca.com

## 📚 Documentation

- [Architecture Decision Records](https://github.com/jolarca-dev/jolarca-infrastructure/tree/main/docs/adr)
- [Threat Model](https://github.com/jolarca-dev/jolarca-infrastructure/blob/main/docs/threat-model.md)
- [Isolation Model](https://github.com/jolarca-dev/jolarca-infrastructure/blob/main/security/isolation-model.md)

## 🤝 Contributing

We follow **Conventional Commits** and enforce:

- Pre-commit hooks (gitleaks, terraform fmt, checkov)
- Two-person rule for security-sensitive paths
- Plan-first change management (no direct pushes to main)

See `CONTRIBUTING.md` in each repository for details.

---

<p align="center">
  <strong>Built with paranoia. Shipped with confidence.</strong>
</p>
