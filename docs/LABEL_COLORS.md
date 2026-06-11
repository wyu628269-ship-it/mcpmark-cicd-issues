# Label Organization Guide

This document is the single source of truth for **label documentation** in this repository. It enumerates every existing label, groups them by category, and provides usage guidelines so that contributors and maintainers can apply labels consistently. A well-maintained **label guide** improves the **visual organization** of the issue tracker, makes triage faster, and gives us a reliable foundation for automation.

## Label Categories

The following table groups every label currently present in the repository into intuitive categories. Use it as a quick reference when creating or triaging issues.

| Label Name | Category | Description |
|------------|----------|-------------|
| bug | issue-type | Something isn't working. Use for confirmed defects, broken behavior, regressions, and unexpected crashes. |
| enhancement | issue-type | New feature or request. Use for net-new functionality, user-facing improvements, and feature enhancements. |
| epic | issue-type | Large feature that requires multiple sub-tasks. Use to track a parent initiative that is broken down into smaller issues. |
| maintenance | issue-type | Maintenance and housekeeping tasks. Use for dependency updates, refactoring, code cleanup, and routine upkeep. |
| documentation | issue-type | Documentation improvements. Use for additions, edits, or fixes to docs, READMEs, and in-code comments. |
| priority-critical | priority | Critical priority. Use for production-blocking issues, security incidents, or outages that need immediate attention. |
| priority-high | priority | High priority. Use for important issues that should be addressed soon, typically assigned to a near-term milestone. |
| priority-medium | priority | Medium priority. Use for normal-priority issues that are useful but not urgent. This is the default priority. |
| priority-low | priority | Low priority. Use for nice-to-have improvements, minor issues, and non-blocking follow-ups. |
| needs-triage | status | Needs maintainer review. Applied automatically when an issue is opened and awaits initial categorization. |
| needs-review | status | Awaiting review. Applied after initial triage to indicate the issue is ready for maintainer or peer review. |
| first-time-contributor | status | First-time contributor. Applied to issues or PRs from authors making their first contribution to this repository. |

## Usage Guidelines

The categories above are designed to be orthogonal: an issue should typically carry **one label from each category** (one issue-type, one priority, and one status) so that filtering and reporting remain meaningful. Below are the rules of thumb for applying each category.

### Issue Type (`issue-type`)
Apply exactly one `issue-type` label to every new issue. Choose the closest match for what the issue is *about*:
- `bug` — for confirmed defects. Always include reproduction steps.
- `enhancement` — for new features or improvements to existing features.
- `epic` — for large initiatives that will spawn multiple sub-issues. Epics should be broken down promptly.
- `maintenance` — for refactors, dependency updates, and housekeeping that don't change user-visible behavior.
- `documentation` — for any change primarily about documentation, including this very guide.

### Priority (`priority`)
Apply exactly one `priority-*` label to every new issue. Priority communicates *urgency* and influences milestone assignment:
- `priority-critical` — production is broken or a security issue is present. Page on-call.
- `priority-high` — important and time-sensitive. Should land in the current or next milestone.
- `priority-medium` — the default. Work it into a near-future milestone.
- `priority-low` — nice-to-have. Triage and schedule as capacity allows.

### Status (`status`)
Status labels track the **lifecycle** of an issue and are usually applied by automation, not by the author:
- `needs-triage` — initial state for newly opened issues, indicating a maintainer must review and classify them.
- `needs-review` — the issue has been triaged and is awaiting implementation review or design review.
- `first-time-contributor` — informational label that highlights a contribution from a new community member, helping maintainers prioritize welcoming responses.

### General Rules
- **One per category** by default. If an issue genuinely needs more than one label from the same category, leave a comment explaining why.
- **Prefer existing labels**. If a new label is required, open an issue first to discuss and update this guide in the same change.
- **Keep descriptions accurate**. If you change a label's meaning, update this **label guide** in the same PR so that the **organization** of the issue tracker stays consistent.
- **Use for visual organization**. A consistent label set is what makes the issue list scannable at a glance — pick the label that best summarizes the issue's current state.

A well-followed **label guide** is the foundation of clean **label documentation** and a pleasant **visual organization** experience for everyone who interacts with this repository.
