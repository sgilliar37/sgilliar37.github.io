# GridPilot for Jira User Manual

GridPilot for Jira gives teams a spreadsheet-like way to query, organize, edit, save, share, export, and analyze Jira issue data without leaving Jira.

## Getting Started

Open **GridPilot for Jira** from the Jira app navigation. The main screen contains the configuration controls, query results, saved view tools, collection tools, and pivot table options.

Use the **Trust** shield in the top toolbar to see a brief summary of how the app handles Jira data and saved configuration.

## Running a Query

1. Enter or select a JQL query.
2. Choose the Jira fields you want to display as columns.
3. Optionally select grouping fields.
4. Click **Run Search**.

GridPilot displays the matching Jira issues in the results area.

## Query Results

The query results grid lets you:

- View Jira issues in rows and selected fields in columns.
- Open an issue by clicking the issue key or summary.
- Resize columns by dragging column edges.
- Sort columns by clicking column headers.
- Manually reorder rows by dragging rows.
- Expand parent issues to show subtasks when available.
- Hide or show completed issues.
- Switch between standard grouped results and grid results.
- Use fullscreen mode for more workspace.

### Column Sorting and Manual Row Order

Click a column header to sort results by that column. Click the same header again to switch between ascending and descending order.

If you manually move rows, GridPilot preserves your manual row order and pauses column sorting. To return to column sorting, either:

- Click a column header, or
- Click **clear manual order** in the manual-order notice.

## Editing Jira Fields

Editable fields can be updated directly from the results grid.

1. Click an editable cell.
2. Change the value.
3. Use the field's normal save behavior, or click away after making a change to save it.

If you click away from a field without changing anything, the editor closes without saving.

Press **Escape** while editing to cancel the edit without saving. In fullscreen mode, the first Escape cancels the active field edit; when no field is being edited, Escape can exit fullscreen.

Some fields may not be editable because Jira does not allow editing that field for the issue, screen, project, or issue type. GridPilot follows Jira permissions and edit metadata.

## Saved Views

Saved views let you reuse a GridPilot configuration.

A saved view can include:

- JQL
- Selected columns
- Column order
- Grouping
- Formatting rules
- Hide done setting
- Frozen column
- Display preferences

To save a view:

1. Configure the query and results layout.
2. Click the save view action.
3. Choose whether to save a new view or overwrite an existing one.

New saved views start private. Existing views keep their current sharing settings when overwritten.

## Managing Saved Views

Use **Manage Saved Views** to:

- Load a saved view.
- Delete a saved view.
- Manage view permissions.

Deleting a saved view removes only the saved GridPilot configuration. It does not delete or change Jira issues.

## Sharing and Permissions

Saved views and collections can be shared with other users.

Sharing options include:

- **Private**: only the owner can access it.
- **Share with selected users**: selected users can view or edit based on permission.
- **Share with everyone**: anyone who can access the app can view it.

Permission levels:

- **View**: user can load the saved item.
- **Edit**: user can change configuration and sharing.

Sharing a saved GridPilot item does not change Jira project permissions or issue permissions.

## Collections

Collections help organize saved views and pivot tables into groups.

Use collections to:

- Group related saved views.
- Add pivot tables to a collection.
- Open multiple related views as tabs.
- Share a set of reporting or operational views with users.

## Pivot Tables

Pivot tables summarize Jira issue data by rows, columns, values, and aggregations.

Use pivot tables to analyze work by:

- Status
- Assignee
- Priority
- Project
- Issue type
- Custom fields
- Time-based metrics

The default aggregation is **None**, which keeps the initial pivot output close to the query results until you choose a summary option.

Pivot tables can be saved and added to collections.

## Formatting Rules

Formatting rules help highlight important issues or fields.

Use formatting to visually flag items based on field values, such as:

- High priority issues
- Blocked work
- Aging issues
- Specific statuses
- Empty or populated fields

Formatting can apply to rows or individual fields, depending on the rule.

## Exporting Results

Click **Export CSV** to download the currently visible results.

The export includes:

- Visible result rows
- Selected columns
- Issue URLs
- Current grouping context

Exports use what is visible in the grid at the time of export.

## Bulk Edit

Click **Bulk edit** to open Jira's native bulk edit flow for the current result set.

Jira applies its normal project, issue, and field permissions before allowing changes.

## Fullscreen Mode

Use fullscreen mode when you need more room for large result sets or wide tables.

While editing a field in fullscreen:

- Press **Escape** once to cancel the field edit.
- Press **Escape** again, when no field is being edited, to exit fullscreen.

## Data and Trust Notes

GridPilot runs on Atlassian Forge. Jira issue data is requested using the current user's Jira permissions.

Saved GridPilot configuration is stored in Forge app storage. Some low-sensitivity UI state may be cached locally in the browser for resilience and convenience.

GridPilot does not replace Jira permissions. If a user cannot view or edit an issue in Jira, GridPilot should not grant access to that issue or edit.

## Troubleshooting

### I cannot edit a field

The field may not be editable for that issue in Jira. Confirm the field is available on the issue's Edit screen and that you have permission to edit the issue.

### My column sorting stopped working

You may have manually moved rows. Manual row order pauses column sorting. Click a column header or click **clear manual order** to return to column sorting.

### My saved view is read-only

You may have view-only access to a shared view. Ask the owner to grant edit access if you need to change the saved configuration.

### A query returns no results

Check that the JQL is valid and that your Jira permissions allow you to view matching issues.

### Export does not include expected rows

The CSV export uses the currently visible results. Refresh or rerun the query, adjust filters, and verify grouping or hidden done settings before exporting.

