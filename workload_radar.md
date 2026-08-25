What it is
Team Workload shows how much open work each person is carrying across every team — not just what they are assigned, but everything where they are named as the Developer, Tester, or Designer too. That union is something no stock Jira report can group by, and it is the whole point of the app: spot who is overloaded, what is blocked, and what has gone stale.

It comes in two places: a compact dashboard gadget (a top-N view you add to a Jira dashboard) and the full-width Workload Radar page (everyone), reached from the Apps menu. Both show the same numbers.

Quick start
Open the Workload Radar page from the Jira Apps menu, or add the Team Workload gadget to a dashboard.
Each row is a person; the badges on the right summarise their open work.
Click a row to expand every ticket they are on.
Click a ticket key to open it and edit fields inline.
Narrow the view with the project filter, Open sprint toggle, and the search box; re-order with the Open / capacity sort.
Switch light/dark with the theme button next to the title.
Settings (admin)
Open Settings from the gear icon in the header. These are shared across the whole site, so only a Jira administrator can change them — everyone else sees them read-only. Each change records who made it and when.

Capacity field (the “developer” field). The one field the capacity number counts per person — your “who is carrying the most development work” metric. Defaults to the Developer field; pick any user field (e.g. a differently-named “Engineer” field) to count that instead.
Role fields — Developer, Tester, Designer. Map each role to the Jira field that names that person on a ticket. Choose a field, or leave it “Not tracked” if your site does not use that role — a “Not tracked” role is neither counted nor reported as missing. A role you never touch is auto-detected by field name, so most sites need no setup here.
Stale after (days). A ticket nobody has touched in this many days counts as stale. Leave blank to use the default of 7.
Tip: if you see a yellow “not counted” notice, an admin can point the matching role field here to start counting it — or dismiss the notice with its ✕.


Each person's row ends in these totals. Capacity counts only the chosen field (e.g. Developer); open is everything they are on.
Capacity — open tickets that name the person in the chosen capacity field.
Open — every unfinished ticket they are on (assignee ∪ the role fields).
In progress / To do — split of the open total by status category.
Blocked — tickets flagged/blocked.
Stale — untouched for at least the stale threshold.
Team chips under a name show which teams the person's work spans — click a chip to filter their tickets to that team. Re-order the whole list with the Open / capacity sort toggle. Narrow scope with the project filter, Open sprint (only work in an active sprint), and the search box (matches people and team names). Your filter, sort, and theme choices are remembered per browser.

Opening & editing a ticket
Click a ticket key to open the details modal. It shows every field, with read-only ones displayed for context. Click any editable field to edit it in place — it saves when you click away or press Enter, exactly like Jira's own inline edit. Descriptions and comments render as rich text.

Close the modal with the ✕ in the top corner. Pressing Esc or clicking the backdrop is intentionally disabled so a stray key never discards an edit in progress. Every read and edit runs as you, so Jira enforces your own permissions — you can only change what you could change in Jira directly.

Tips & FAQ
Why is someone counted on a ticket they are not assigned to? Because they are named as its Developer, Tester, or Designer. Counting that hidden load is the reason the app exists.
Who can see what? The app runs as the viewing user, so you only ever see — and edit — the work you can already access in Jira. It adds no privilege of its own.
What does it store? No issue data. Reports are computed live from Jira and discarded; only the admin settings above are saved (in Atlassian's own storage, no external service).
Gadget vs page. The gadget is a compact top-N view for a dashboard; the Workload Radar page lists everyone with room for the per-person expansion.
