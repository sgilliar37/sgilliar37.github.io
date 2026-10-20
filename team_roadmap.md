**Team Roadmap**

What it is:

Team Roadmap gives you one holistic, cross-project roadmap for Jira — every project you care about on a single timeline, instead of one project's board at a time. It is built to be cleaner and easier to read than Jira's built-in roadmap: the work that matters, its progress, its target dates and its risks, all in one place so leaders can actually see where things stand across the portfolio.

It shows up in four places, all read from the same live Jira data: the full-width Team Roadmap page (from the Apps menu), an admin settings page, a read-only Jira dashboard gadget, and a read-only Confluence macro you embed on a page. The gadget and macro hide the editing and what-if controls so the roadmap can be shared safely with a wider audience.

Quick start:

Open the Team Roadmap page from the Jira Apps menu.
Pick the projects (or a saved roadmap) you want to see; each row is an epic or initiative with its progress, target date and status.
Click a row to expand the work beneath it; click a ticket key to open and edit it inline.
Narrow the view with the project filter, the search box and the status filters; your choices are remembered per roadmap.
Switch light/dark with the theme button next to the title.

Working with the roadmap:

Timeline & sprints — work is laid out on a timeline with its target dates, and active and future sprints are drawn alongside so you can see what is scheduled when.
Progress — every row rolls up the completion of the work beneath it, so a parent shows how far along its children are.
Portfolio trends — compact trend tiles show how each area's completion is moving since the last period, up or down, at a glance.
Baselines — snapshot the plan on demand, then compare where things are now against where you said they would be. Useful before a planning cycle or a stakeholder review.
Commit the forecast — turn a projected finish date into committed target dates on the underlying tickets in a click.
Ask the roadmap — ask a plain-language question and get an answer drawn from your live roadmap (AI; admin-controlled and off until an admin turns it on).
Share & embed — a read-only share for stakeholders, plus the dashboard gadget and Confluence macro so people see the roadmap where they already work.
Weekly digest — a once-a-week summary of what moved, what is newly at risk and what is overdue for a check-in.

Inline editing:

Click a ticket key to open its details. Click any editable field — Status, Priority, Owner, Target date — to change it in place; it saves when you click away or press Enter, exactly like Jira's own inline edit. Every read and edit runs as you, so Jira enforces your own permissions: you can only change what you could change in Jira directly. The owner picker lists the people Jira says can be assigned the issue.

Settings (admin):

Open Settings from the Team Roadmap settings admin page. These settings are shared across the whole site, so only a Jira administrator can change them.

Ask the roadmap (AI). Off by default. An admin turns it on and chooses the model. When on, everyone who can see the roadmap can ask questions; the questions and the roadmap's own tickets are read as the asker and answered by a Claude model running on Atlassian's Forge LLM — nothing leaves your Atlassian environment. Usage is billed in Atlassian's Forge LLM credits.

Tips & FAQ:

Who can see what? The app runs as the viewing user, so you only ever see — and edit — the work you can already access in Jira. The read-only gadget, macro and share show only what their viewer can already see. The app adds no privilege of its own.
What does it store? Your roadmap configuration, any baselines you capture, and the weekly digest — all in Atlassian's own Forge app storage. Live roadmaps are computed from Jira on the fly and discarded. No issue data is sent to any outside service.
Does it send my data anywhere? No. Team Roadmap has no external egress — it is eligible for Atlassian's Runs on Atlassian program. Everything stays inside your Atlassian tenant, isolated per installation.
Page vs gadget vs macro. The page is the full editable roadmap; the dashboard gadget and Confluence macro are read-only embeds of the same roadmap for sharing.
