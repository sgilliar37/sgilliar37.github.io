## Security Policy – Team Roadmap for Jira

### Overview

Security is a core priority of Team Roadmap for Jira. The application is built entirely on Atlassian Forge and is eligible for Atlassian's **Runs on Atlassian** program, meaning it has no external egress — your data never leaves your Atlassian environment.

---

### Authentication & Authorization

- Jira and Confluence access is handled via Atlassian Forge permissions
- All reads and writes run as the current user, so Jira enforces that user's own permissions
- The App grants no privilege of its own; you only ever see and edit what you already can in Jira
- Administrator-only settings (including the AI feature) are gated to Jira administrators and verified server-side

---

### Data Protection

- All communication is encrypted via HTTPS (TLS 1.2+), managed by Atlassian Forge
- No sensitive credentials are stored by the App
- Configuration, baselines and digests are kept in Forge app storage, isolated per installation
- No data is sent to any service outside the Atlassian environment

---

### Input Validation

- JQL is constructed with proper quoting and validated issue keys to prevent query injection
- Input used in AI prompts is neutralized before use
- Output is rendered without unsafe HTML, `eval`, or dynamic code execution

---

### Least Privilege Access

The app only requests the minimum scopes required:

- Read Jira work (to build the roadmap)
- Write Jira work (only for inline edits you make, as you)
- Read Jira users (to populate the owner picker)
- Read boards and sprints (to show sprints on the timeline)
- App storage (for configuration, baselines and digests)

---

### Infrastructure

- Hosted entirely on Atlassian Forge
- No external servers, no external egress, no direct database exposure
- Per-tenant isolation provided by the Forge platform
- Any AI processing runs on Atlassian's Forge LLM, within Atlassian's infrastructure

---

### Monitoring & Logging

- Errors and events are logged for debugging
- Logs do not contain sensitive data
- Suspicious activity can be investigated

---

### Incident Response

In the event of a security issue:

- Immediate investigation will be performed
- Affected users will be notified if necessary
- Fixes will be deployed promptly

---

### Responsible Disclosure

If you discover a vulnerability, please contact:

sgilliar37@yahoo.com
