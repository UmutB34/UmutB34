# Portfolio Roadmap

Working plan for turning this GitHub account into a professional technical portfolio
that supports applications for IT Manager / Head of IT / Infrastructure / Technology
Operations leadership roles.

Last reviewed: 2026-09-30

---

## 1. Current public repository audit

Public repositories owned by `UmutB34` at the time of review: **2**.

| Repository | Content | Classification | Notes |
|---|---|---|---|
| `UmutB34` | Profile README | **KEEP** | Now carries the professional profile. |
| `Vmware` | Single text file (`vmwk17key.txt`) copied from a public gist, listing VMware Workstation license keys | **ARCHIVE CANDIDATE — remove (urgent)** | See finding below. |

### Evaluation

| Criterion | `UmutB34` | `Vmware` |
|---|---|---|
| Professional relevance | High | None |
| Code / documentation quality | Profile README only | No README, no code |
| Security | Clean | Distributes third-party license keys |
| Activity | Active | Untouched since 2024-06 |
| Career relevance | High | Negative |
| Technical credibility | Positive | Negative |

### Finding: `Vmware` repository (high priority)

The repository publicly redistributes software license keys that were copied from
someone else's gist, including third-party links and promotional text.

For a profile positioned toward IT management — a role that typically owns software
licensing compliance — this is a reputational and compliance risk, and it is
the first thing a reviewer will see in the repository list.

Also note: VMware Workstation Pro is free for personal use (Broadcom, 2024), so the
file has no remaining practical value.

**Recommended action (owner decision):** delete the repository, or at minimum make it
private. Archiving alone is not enough — archived repositories remain public.
This has not been changed automatically.

---

## 2. Recommended pinned repositories

Today only the profile repository is suitable for pinning. Pin showcase repositories
as they are published (section 3), in this order of priority:

1. `enterprise-infrastructure-lab`
2. `security-operations-toolkit`
3. `enterprise-it-operations`
4. `automation-toolkit`
5. `architecture-notes`

Leave `Vmware` unpinned and remove it.

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

1. Remove or make private the `Vmware` repository.
2. Pin the profile repository; add pins as showcase repositories are published.
3. Publish `enterprise-infrastructure-lab` first — it best proves hands-on depth.
4. Publish `security-operations-toolkit` with 2–3 small, well-documented defensive checks.
5. Add `architecture-notes` with the first sanitized ADRs (e.g. network segmentation, backup strategy).
