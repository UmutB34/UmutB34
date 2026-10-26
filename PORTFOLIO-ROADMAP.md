# Portfolio Roadmap

Working plan for turning this GitHub account into a professional technical portfolio
that supports applications for IT Manager / Head of IT / Infrastructure / Technology
Operations leadership roles.

Last reviewed: 2026-09-30

---

## 1. Current public repository audit

Public repositories owned by `UmutB34` after cleanup (2026-09-30): **1**.

| Repository | Content | Classification | Notes |
|---|---|---|---|
| `UmutB34` | Profile README | **KEEP** | Carries the professional profile. |

A legacy repository with no portfolio value was removed on 2026-09-30.

---

## 2. Recommended pinned repositories

Today only the profile repository is suitable for pinning. Pin showcase repositories
as they are published (section 3), in this order of priority:

1. `enterprise-infrastructure-lab`
2. `security-operations-toolkit`
3. `enterprise-it-operations`
4. `automation-toolkit`
5. `architecture-notes`

---

## 3. Future portfolio architecture (proposed — not yet created)

| Repository | Purpose | Classification |
|---|---|---|
| `enterprise-infrastructure-lab` | Enterprise-style infrastructure architecture patterns | PORTFOLIO CANDIDATE |
| `enterprise-it-operations` | Runbooks and operational patterns | PORTFOLIO CANDIDATE |
| `security-operations-toolkit` | Safe, defensive utilities | PORTFOLIO CANDIDATE |
| `automation-toolkit` | Administration and operations scripts | PORTFOLIO CANDIDATE |
| `architecture-notes` | Sanitized diagrams and decision records | PORTFOLIO CANDIDATE |

### `enterprise-infrastructure-lab`

Documents the lab as enterprise architecture patterns, not as a hobby build log.

- Proxmox virtualization and resource design
- Windows Server and Linux service roles
- Network segmentation and firewall policy design
- Monitoring and alerting
- Backup and restore testing
- Identity services

### `enterprise-it-operations`

- Runbooks (onboarding / offboarding, patching, incident first response)
- Incident handling and post-incident review templates
- Change management process and templates
- Asset lifecycle (procurement → deployment → retirement)
- Monitoring and service operations patterns

### `security-operations-toolkit`

Defensive, read-only utilities only. No offensive tooling.

- DNS inspection
- TLS / certificate checks
- HTTP security header checks
- Domain / email posture checks (SPF, DMARC)
- Log parsing and health checks

### `automation-toolkit`

PowerShell, Python and Bash focused on:

- Administration and health checks
- Inventory and reporting
- Routine operational automation

### `architecture-notes`

Sanitized architecture diagrams and Architecture Decision Records (ADRs):

- Network architecture
- Identity
- Endpoint management
- Business continuity
- Monitoring
- Security architecture
- Hybrid infrastructure

---

## 4. Repository quality standard

Every showcase repository should eventually contain:

```text
README.md
docs/
examples/
LICENSE            (where appropriate)
.gitignore
SECURITY.md        (where relevant)
```

README structure:

1. Problem
2. Architecture
3. Technology
4. Implementation
5. Security Considerations
6. Operational Considerations
7. Lessons Learned

### Sanitization rules (apply to every repository)

Never publish, even from past employers or the lab:

- IP addresses, internal DNS names or internal domains
- Credentials, API keys, tokens, private keys, license keys
- Tenant IDs or other identifiers
- Employee, customer or company names from internal environments
- VPN, firewall rule sets or production topology
- Internal screenshots

Use placeholders (`example.com`, RFC 5737 documentation ranges such as
`192.0.2.0/24`, `CONTOSO`) and run a secret scan (e.g. `gitleaks`) before every push.

---

## 5. Next actions

1. Pin the profile repository; add pins as showcase repositories are published.
2. Publish `enterprise-infrastructure-lab` first — it best proves hands-on depth.
3. Publish `security-operations-toolkit` with 2–3 small, well-documented defensive checks.
4. Add `architecture-notes` with the first sanitized ADRs (e.g. network segmentation, backup strategy).
5. Publish `enterprise-it-operations` with the first runbooks and change templates.
