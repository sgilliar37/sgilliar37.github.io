## Compliance & CSA CCM-Lite / CAIQ-Lite v4 Coverage – Team Roadmap for Jira

### Overview

This document maps **Team Roadmap for Jira** to the Cloud Security Alliance (CSA) **Cloud Controls Matrix (CCM) v4** and its streamlined **CCM-Lite / CAIQ-Lite v4** assessment, which covers **17 control domains**. It is a vendor self-assessment, provided for transparency to administrators and security reviewers.

Team Roadmap is an **Atlassian Forge** app. It runs entirely on Atlassian's cloud platform, stores data only in Atlassian-provided storage, and has **no external egress** — it is eligible for Atlassian's **Runs on Atlassian** program. Because of this, the assessment follows a **shared-responsibility model**:

- **Inherited** controls are provided by the underlying cloud platform, **Atlassian Cloud / Forge**. Atlassian maintains SOC 2, ISO/IEC 27001 and 27018, and a CSA STAR registration; those certifications cover the infrastructure, datacenter, platform cryptography, and physical controls this app relies on.
- **App (vendor)** controls are the responsibility of Team Roadmap and are described below.

Status key: **Covered** (app-level control in place) · **Inherited** (provided by Atlassian/Forge) · **Partial** (basic control appropriate to the app's scope) · **N/A** (not applicable to this app).

---

### Domain-by-domain coverage

**A&A — Audit & Assurance** · *Covered / Inherited*
Platform certifications (SOC 2, ISO 27001/27018, CSA STAR) are inherited from Atlassian. At the app level, every release passes an automated quality and security gate (static analysis with a SonarQube "A" rating on Security, Reliability, Security Hotspots and Maintainability; full unit-test suite; dependency audit) and a documented OWASP- and Marketplace-aligned security review before deployment.

**AIS — Application & Interface Security** · *Covered*
Secure SDLC with automated static analysis and tests on every change. Input is validated and encoded: JQL is built with proper quoting and validated issue keys to prevent query injection; input to AI prompts is neutralized; output is rendered without `innerHTML`, `eval`, or dynamic code execution. All API access is over TLS (handled by Forge). The app exposes no public endpoints of its own.

**BCR — Business Continuity & Operational Resilience** · *Inherited*
The app is stateless compute plus Atlassian-managed storage; it operates no infrastructure of its own. Availability, backup, and disaster recovery are provided by the Atlassian Forge platform. Loss of the app does not affect the customer's Jira data, which remains in Jira.

**CCC — Change Control & Configuration Management** · *Covered*
All changes are version-controlled in git and must pass automated gates (static analysis, tests, convention checks) before release. Forge provides versioned, auditable deployments; any change to permission scopes requires each site administrator to review and re-consent on upgrade.

**CEK — Cryptography, Encryption & Key Management** · *Inherited*
Encryption in transit (TLS 1.2+) and at rest is provided by the Atlassian Forge platform. The app stores no secrets, manages no cryptographic keys, and handles no credentials.

**DCS — Datacenter Security** · *Inherited*
The app operates no datacenters. All physical and environmental controls are provided by Atlassian's cloud infrastructure.

**DSP — Data Security & Privacy Lifecycle Management** · *Covered*
Strong data minimization: live roadmaps are computed from Jira on demand and discarded; only roadmap configuration, on-demand baselines (a compact key/target/progress summary, not full issue content), and the weekly digest are stored, in Forge app storage. No data leaves the Atlassian tenant; there is no external analytics or tracking. Data is isolated per installation and deleted on uninstall or on request. A published Privacy Policy describes processing.

**GRC — Governance, Risk & Compliance** · *Covered / Partial*
Published Privacy Policy, Security Policy, Terms of Service, and this compliance mapping. A documented security review is performed against OWASP and the Atlassian Marketplace security requirements. Broader organizational governance (formal risk register, enterprise policy set) is scoped to the app's size and supplemented by inherited Atlassian controls.

**HRS — Human Resources Security** · *Inherited / N/A*
Personnel controls (screening, training, onboarding/offboarding) for the platform are provided by Atlassian. The app involves no sub-processors with access to customer data.

**IAM — Identity & Access Management** · *Covered*
The app holds **no identity of its own and creates no accounts**. Every read and write runs as the **current Jira user** (`asUser`), so Jira enforces that user's own permissions — the app grants no additional access. Administrator-only settings (including the optional AI feature) are gated to Jira administrators and verified server-side. End-user authentication, SSO, and MFA are inherited from the Atlassian/Jira identity platform. Scopes follow least privilege (see STA).

**IPY — Interoperability & Portability** · *Covered*
Customer data stays in Jira in its native form and is accessed through standard, documented Atlassian REST APIs — there is no proprietary data lock-in. App-stored configuration and baselines are removed when the app is uninstalled.

**IVS — Infrastructure & Virtualization Security** · *Inherited*
The app runs on Forge's managed serverless runtime (Node.js). It provisions and manages no infrastructure, networks, or virtual machines; all such controls are provided by Atlassian.

**LOG — Logging & Monitoring** · *Covered / Partial*
Application errors and events are logged for diagnostics without sensitive data. Platform-level logging, monitoring, and alerting are inherited from Atlassian Forge.

**SEF — Security Incident Management, E-Discovery & Cloud Forensics** · *Covered / Inherited*
A responsible-disclosure contact is published and a basic incident-response process (investigate, notify affected users if needed, deploy fixes promptly) is documented in the Security Policy. Platform-level incident detection and response are inherited from Atlassian.

**STA — Supply Chain Management, Transparency & Accountability** · *Covered*
Minimal, pinned third-party dependencies, scanned with a dependency audit and static application security testing (SAST) in the release gate. The only platform dependency is Atlassian (Forge, Jira, Confluence); there are **no other sub-processors** and no external services. This document and the published policies provide transparency.

**TVM — Threat & Vulnerability Management** · *Covered*
Static analysis (SAST) and dependency vulnerability auditing run on every release; findings are resolved before deployment (no suppressions). The app follows OWASP guidance and accepts vulnerability reports via the published disclosure contact. Platform patching is inherited from Atlassian.

**UEM — Universal Endpoint Management** · *Inherited / N/A*
The app manages no endpoints and runs on Forge's serverless platform; there is no app-managed device fleet. Platform and developer-endpoint controls are provided by Atlassian and the vendor respectively.

---

### Shared-responsibility summary

| Responsibility | Examples | Owner |
| --- | --- | --- |
| Physical / datacenter, infrastructure, virtualization, platform encryption, BC/DR, endpoint, HR | DCS, IVS, CEK, BCR, UEM, HRS | **Atlassian (inherited)** |
| Application security, access enforcement, data minimization, change control, dependency & vulnerability management, incident disclosure, transparency | AIS, IAM, DSP, CCC, STA, TVM, SEF, GRC, A&A, IPY, LOG | **Team Roadmap (app)** |

### Scope & data footprint (for reviewers)

- **Permissions (least privilege):** read Jira work, write Jira work (only for edits you make, as you), read Jira users (owner picker), read boards and sprints (timeline), and app storage. No other scopes; no egress permissions.
- **Data stored:** roadmap configuration, baselines (compact summaries), weekly digest — in Forge app storage, isolated per installation.
- **Data not stored or transmitted externally:** full issue content, passwords, payment data, and any third-party analytics. The app sends nothing outside the Atlassian environment.
- **AI ("Ask the roadmap"):** optional, off by default, admin-enabled; runs on Atlassian's Forge LLM, within Atlassian's infrastructure.

### Contact

For compliance inquiries:

**Email:** sgilliar37@yahoo.com

*This self-assessment references the CSA CCM / CAIQ domain framework for structure. It does not reproduce the CSA CCM-Lite / CAIQ-Lite questionnaire, which is published by the Cloud Security Alliance at cloudsecurityalliance.org.*
