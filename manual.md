# Release Scheduler User Manual

Version: April 20, 2026  
Audience: Release Managers, Approvers, Team Leads, and Jira Admins

## 1. What this app does

Release Scheduler is a Jira Forge app that helps teams plan, coordinate, and deliver releases from one place. It combines release tracking, issue-level visibility, approvals, scheduling, notifications, and reporting.

### Key outcomes for users
- Plan releases with clear owners, dates, and participants.
- Track readiness with progress and risk-oriented signals.
- Manage release tickets in-place (expand, review, add, remove, move).
- Coordinate approvals and deployment notifications (Slack supported).
- Publish release dashboards to Confluence and export PDF snapshots.
- Review history in released views and calendar timelines.

## 2. Main areas of the app

### Release page (global/project view)
Primary workspace for release operations.

- Unreleased: active planning and execution.
- Released: historical/audit view of completed releases.
- Calendar: date-based timeline for schedule visibility.

### Admin page
Configuration center for app defaults and integrations.

- Notification provider and templates.
- Default timezone and project settings.
- Slack user mapping.
- Delegated app admins.
- Optional GitHub settings.

## 3. Roles and permissions

### Release Manager
Can create/edit releases, manage scope, run approvals, send notifications, and mark releases complete.

### Approver
Can review assigned releases and record approval decisions.

### Viewer/Stakeholder
Can track release health, scope, dates, and status without changing configuration.

## 4. Daily workflow (recommended)

1. Open **Unreleased** view.
2. Create or select a target release.
3. Set schedule details (start, staging, production, release date).
4. Add people involved and release driver.
5. Expand release row to validate Jira ticket scope.
6. Add approvers and notify when ready.
7. Monitor readiness and blockers.
8. Mark release complete when deployed.
9. Publish summary to Confluence or export PDF.

## 5. Core features and how to use them

## 5.1 Create and edit releases
- Use **Create Release** to initialize a new release version.
- Edit release metadata any time (dates, owner/driver, people, notes).
- Keep names consistent so teams can find releases quickly.

## 5.2 Expand/collapse ticket view (no context loss)
- Expand a release row to see all associated Jira tickets inline.
- Collapse when done; no page refresh is required.
- Add/remove/move tickets directly from the same workflow.

## 5.3 Readiness and progress
- Progress shows done/total issue status for each release.
- Readiness indicators help identify if deployment is near-ready.
- Use issue details to locate blockers before staging/production.

## 5.4 Approvals
- Assign one or more approvers to a release.
- Approvers can record decision status (approve/decline).
- Release managers can track approval completion in one place.

## 5.5 Staging and deployment coordination
- Mark releases with staging and production timing.
- Set users involved so coordination is clear.
- Trigger notifications when release is ready to deploy.

## 5.6 Slack notifications
- Send release notifications to configured channels/users.
- Use templates for standardized communication.
- Scheduled reminders can run automatically around target windows.

## 5.7 Confluence publishing and PDF export
- Save release dashboard details to Confluence for sharing.
- Export PDF snapshots for stakeholder updates and records.

## 5.8 Bundles and cross-project planning
- Group related releases into bundles for coordinated windows.
- Review dependencies, late additions, priority, and story points.
- Use bundle views to drive multi-team release alignment.

## 5.9 Calendar view
- Visual timeline of release and deployment dates.
- Useful for conflict detection and planning cadence.

## 6. Admin setup checklist

1. Open the Admin page.
2. Set default timezone.
3. Configure default project(s).
4. Configure Slack integration and templates.
5. Add Jira-to-Slack user mappings.
6. Confirm delegated app admins.
7. (Optional) Configure GitHub integration.
8. Run a test notification and test Confluence post.

## 7. Troubleshooting quick guide

### No releases shown
- Clear name/date filters.
- Verify selected project scope.
- Refresh the page data.

### Readiness seems inaccurate
- Expand row and verify ticket membership.
- Confirm status transitions are up to date.
- Refresh after major edits.

### Notifications not arriving
- Check Slack webhook/token/channel in Admin settings.
- Verify user mappings for mentions.
- Confirm release has valid staging/production schedule data.

### Confluence post fails
- Verify space selection and permissions.
- Recheck app configuration and retry publish.

## 8. Best practices

- Keep release metadata current, not only on release day.
- Standardize naming for searchability.
- Add approvers early and notify with context.
- Validate ticket scope before final approval.
- Use calendar + bundle views for cross-team conflict prevention.
- Publish post-release summaries to Confluence for traceability.

## 9. Why teams adopt this app

Release Scheduler reduces manual coordination and fragmented tooling by placing planning, approval, communication, and reporting in one Jira-native workflow. In short: less context switching, better release visibility, and faster, lower-risk delivery.
