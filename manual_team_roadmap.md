# Team Roadmap for Jira User Manual

Team Roadmap for Jira brings all of your Jira projects onto one clean, cross-project timeline — a holistic portfolio roadmap that is faster and easier to read than Jira's built-in roadmap. Plan across projects, track progress and risk, capture baselines, forecast delivery, and share a read-only view with stakeholders, all without leaving Atlassian.

## Getting Started

Open **Team Roadmap** from the Jira app navigation (the Apps menu). The main page shows your cross-project roadmap: rows of epics and initiatives on a timeline, each with its progress, target date and status.

The same roadmap is also available, read-only, as a **Jira dashboard gadget** and a **Confluence macro**, so you can place it where your team and leaders already work.

## Reading the Roadmap

Each row represents a piece of work (typically an epic or initiative) and shows:

- Its summary and key.
- A progress roll-up of the work beneath it.
- Its target date on the timeline.
- Its status and priority.
- Risk and schedule signals where applicable.

Click a row to expand the work beneath it. Click a ticket key to open its details.

Active and future sprints are drawn on the timeline so you can see what is scheduled and when.

## Filtering and Finding Work

Narrow the roadmap with:

- **Project filter** — limit the roadmap to specific projects.
- **Search box** — match on summary or key.
- **Status filters** — focus on work in a particular state.

Your filter, sort and theme choices are remembered **per roadmap**, so each roadmap reopens the way you left it. Switch between light and dark with the theme button next to the title.

## Editing Jira Fields

Editable fields can be updated directly from a ticket's details.

1. Click a ticket key to open its details.
2. Click an editable field — Status, Priority, Owner, or Target date.
3. Change the value; it saves when you click away or press Enter.

The Owner picker lists the people Jira says can be assigned the issue. Some fields may not be editable because Jira does not allow editing that field for the issue, screen, project or issue type. Team Roadmap follows Jira permissions and edit metadata — if you cannot change something in Jira, you cannot change it here.

## Portfolio Trends

Trend tiles summarise how each area's completion is moving over time — up or down since the last period — so you can spot momentum and slippage at a glance without building a report.

## Baselines

A baseline is an on-demand snapshot of the plan.

1. Capture a baseline when you want to mark where the plan stands (for example, at the start of a planning cycle).
2. Later, compare the current roadmap against that baseline to see what has moved — what is ahead, what has slipped, and what has changed scope.

Baselines are stored in Atlassian's Forge app storage. They capture a compact summary of each item (key, target, progress) rather than full issue content.

## Commit the Forecast

When the roadmap projects a finish date for an area, you can **commit the forecast** — turn that projected date into committed target dates on the underlying tickets in a click. The change is written back to Jira as you, subject to your permissions.

## Ask the Roadmap (AI)

If a Jira administrator has enabled it, you can ask the roadmap a plain-language question and get an answer drawn from your live roadmap.

- The feature is **off by default**; an admin turns it on and chooses the model in Settings.
- Your question and the roadmap's tickets are read **as you** and answered by a Claude model running on Atlassian's Forge LLM.
- Nothing is sent to any service outside your Atlassian environment.
- Usage is billed in Atlassian's Forge LLM credits.

## Sharing and Embedding

- **Read-only share** — share the roadmap with stakeholders in a view-only form.
- **Dashboard gadget** — add the Team Roadmap gadget to a Jira dashboard for a read-only view.
- **Confluence macro** — embed the roadmap, read-only, on a Confluence page.

The gadget and macro hide the editing and what-if controls, and they show each viewer only the work that viewer can already see in Jira.

## Weekly Digest

Team Roadmap produces a weekly summary of what moved, what is newly at risk and what is overdue for a check-in, so teams get a regular pulse without opening the app. The digest is filtered to what each recipient can see.

## Settings (Administrators)

Open the **Team Roadmap settings** admin page. Settings are shared across the whole site, so only a Jira administrator can change them.

- **Ask the roadmap (AI)** — turn the AI feature on or off, and choose the model. Off by default.

## Data and Trust Notes

Team Roadmap runs on Atlassian Forge. Jira data is requested using the current user's Jira permissions.

- The app has **no external egress** — it is eligible for Atlassian's **Runs on Atlassian** program. Your roadmap data never leaves your Atlassian tenant.
- Saved configuration, baselines and the weekly digest are stored in Forge app storage, isolated per installation.
- Live roadmaps are computed from Jira on the fly and discarded.
- Some low-sensitivity UI state (your filter, sort and theme choices) may be cached in your browser for convenience.
- Team Roadmap does not replace Jira permissions. If you cannot view or edit an issue in Jira, Team Roadmap does not grant that access.

## Troubleshooting

### I cannot edit a field

The field may not be editable for that issue in Jira. Confirm the field is on the issue's Edit screen and that you have permission to edit the issue.

### My filters reset

Filters are remembered per roadmap in your browser. If browser storage is cleared or you open the roadmap in a different browser or profile, your saved choices will not carry over.

### The AI question box is missing

"Ask the roadmap" is off until a Jira administrator enables it in the Team Roadmap settings admin page.

### A row shows no progress or the wrong dates

Progress and dates are rolled up from the underlying Jira work and its target/date fields. Confirm the child issues and their dates are set in Jira, and that you have permission to see them.

### The gadget or macro shows less than the full page

The gadget and macro are read-only and show each viewer only the work they can already see in Jira. A viewer with narrower permissions sees less.
