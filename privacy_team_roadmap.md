## Privacy Policy – Team Roadmap for Jira

### Overview
Team Roadmap for Jira ("the App") provides a holistic, cross-project roadmap inside Jira. We take user privacy seriously and only process the minimum data necessary to provide the App's functionality. The App has no external egress: it does not send your data to any service outside your Atlassian environment.

---

### Data We Collect

The App may process the following data:

- Jira issue data (issue keys, summaries, statuses, priorities, assignees and the people named on an issue, target/schedule dates, sprint and board data)
- User identifiers (Jira account ID and display name)
- Roadmap configuration, baselines, and the weekly digest that you or your administrators create

---

### Data We Do NOT Collect

We do not collect or store:

- User passwords
- Personal emails beyond what is provided by Jira APIs
- Payment or billing information
- Sensitive personal data
- Any usage analytics or tracking sent to third-party services

---

### How Data Is Used

We use data strictly to:

- Build and display the cross-project roadmap, trends, baselines and forecasts
- Write back edits (status, priority, owner, target dates) to Jira when you make them
- Produce the weekly digest of roadmap activity
- Answer "Ask the roadmap" questions, when an administrator has enabled that feature

---

### Data Storage

- All data is processed and stored using Atlassian Forge infrastructure
- Roadmap configuration, baselines and the weekly digest are stored in Forge app storage, isolated per installation
- Live roadmaps are computed from Jira on demand and are not retained
- Baselines store a compact summary of each item (key, target, progress), not full issue content
- Some low-sensitivity UI preferences (filters, sort, theme) may be cached in your browser

---

### Artificial Intelligence ("Ask the Roadmap")

- This feature is optional and is turned off by default; a Jira administrator must enable it
- When enabled, your question and the relevant roadmap tickets are read using your own Jira permissions and sent to a Claude model hosted on Atlassian's Forge LLM
- This processing takes place within Atlassian's infrastructure; no roadmap data is sent to any service outside your Atlassian environment

---

### Third-Party Services

The App integrates with:

- Atlassian Jira Cloud
- Atlassian Confluence Cloud (for the read-only roadmap macro)

Data is processed only within Atlassian's Forge and cloud infrastructure. The App does not transmit data to any other third party.

---

### Data Retention

- Roadmap configuration, baselines and digests are retained until you delete them or uninstall the App
- No unnecessary long-term storage of issue data is performed
- Data can be deleted upon request

---

### Security

We implement:

- Secure HTTPS communication (handled by Atlassian Forge)
- Jira permission enforcement on every read and write (the App acts as the current user)
- Principle of least privilege for API scopes
- Per-installation tenant isolation provided by Forge

---

### User Control

Users can:

- Revoke access via Jira
- Uninstall the app at any time
- Request data deletion

---

### Contact

For privacy questions:

**Email:** sgilliar37@yahoo.com
