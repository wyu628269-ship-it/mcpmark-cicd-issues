# Label Organization Guide

This document is the single source of truth for all labels used in the
`mcpmark-cicd-issues` repository. It is intended for both new and existing
contributors so that labels are applied consistently, the issue tracker
remains visually organized, and triage stays fast and predictable.

The labels below are grouped into intuitive categories (issue-type,
priority, status, contributor, area, performance) so that it is obvious
which label to reach for when filing, triaging, or routing an issue.
Following this **label guide** ensures reliable **visual organization**,
easier filtering, and a stronger foundation for automation workflows that
rely on label classification.

## Label Categories

| Label Name | Category | Description |
|------------|----------|-------------|
| bug | Issue Type | Something isn't working. Marks a confirmed defect or regression in the codebase. |
| enhancement | Issue Type | New feature or request. Used for incremental improvements, new capabilities, or sub-tasks of an epic. |
| epic | Issue Type | A large feature that should be broken down into multiple sub-tasks. Triggers the issue-automation workflow to create sub-issues. |
| maintenance | Issue Type | Routine maintenance work such as dependency updates, refactoring, or dependency cleanup. |
| question | Issue Type | A question or request for information that does not describe a defect or feature. |
| documentation | Issue Type | Improvements or additions to documentation, guides, or in-code comments. |
| duplicate | Issue Type | Marks an issue that duplicates an existing one. The duplicate should be closed in favor of the original. |
| invalid | Issue Type | The issue does not follow the contribution guidelines or is not actionable. |
| wontfix | Issue Type | This will not be worked on. Used to close issues that are intentionally out of scope. |
| priority-critical | Priority | Production-blocking bugs, outages, or data-loss issues that must be addressed immediately. |
| priority-high | Priority | Important issues that block other work, fix major functionality, or have significant user impact. |
| priority-medium | Priority | Default priority for most issues that are neither critical nor low impact. |
| priority-low | Priority | Nice-to-have improvements, minor issues, or work that can be deferred to a later release. |
| needs-triage | Status | Applied automatically when an issue is first opened and indicates that a maintainer still needs to review it. |
| needs-review | Status | Applied after triage, indicating that the issue is ready for maintainer or contributor review. |
| first-time-contributor | Status | Marks issues opened by a user who has never opened an issue in the repository before. |
| good first issue | Contributor | Good for newcomers. Highlights issues that are approachable for first-time contributors. |
| help wanted | Contributor | Extra attention is wanted. Signals that the maintainers would like community help on this issue. |
| platform-web | Platform | Issues that affect the web front-end or browser-based runtime. |
| platform-api | Platform | Issues that affect the HTTP API, request/response handling, or service endpoints. |
| platform-cli | Platform | Issues that affect the command-line interface, scripts, or terminal tooling. |
| area-frontend | Area | Code, UI, or styling changes that primarily affect the user-facing front-end. |
| area-backend | Area | Changes that primarily affect the server, services, or business logic. |
| area-infrastructure | Area | Changes to CI/CD, deployment, or developer tooling and infrastructure. |
| area-testing | Area | Changes related to test coverage, test infrastructure, or QA processes. |
| performance | Performance | Issues that describe a regression or improvement related to speed, memory, or resource usage. |
| security | Performance | Issues that describe a security vulnerability, hardening task, or compliance requirement. |

## Usage Guidelines

Use the categories below as a quick reference when deciding which label(s)
to apply to a new or existing issue. A single issue can have labels from
multiple categories, but you should usually apply at most one label from
each category unless the situation is exceptional.

### Issue Type

Apply **exactly one** issue-type label to every new issue so that the
intent of the issue is unambiguous. Use:

- `bug` for confirmed defects or regressions.
- `enhancement` for incremental improvements and sub-tasks.
- `epic` for large features that should be decomposed into sub-issues.
- `maintenance` for routine upkeep such as dependency or refactor work.
- `question`, `documentation`, `duplicate`, `invalid`, or `wontfix` for the
  matching special cases.

### Priority

Apply **exactly one** priority label. The default is `priority-medium`.
Escalate to `priority-high` or `priority-critical` for blocking or
production-impacting work. Demote to `priority-low` for nice-to-have
improvements. Issues with `priority-high` or `priority-critical` should
be tracked in the `v1.0.0` milestone.

### Status

Status labels describe the workflow state of the issue. New issues
automatically receive `needs-triage` from the issue-automation workflow.
After a maintainer has reviewed the issue, the workflow transitions the
label to `needs-review`. The `first-time-contributor` label is added
when the author has never previously opened an issue in the repository.

### Contributor

Apply `good first issue` to issues that are approachable for new
contributors and `help wanted` to issues where the maintainers explicitly
want community assistance. These labels are usually combined with an
issue-type and priority label.

### Platform

Use the `platform-*` labels to indicate which runtime or interface the
issue affects. If the issue spans multiple platforms, apply multiple
`platform-*` labels.

### Area

Use the `area-*` labels to indicate which part of the codebase the
change is likely to touch (front-end, back-end, infrastructure, or
testing). Combine with `platform-*` labels when both are useful.

### Performance

Apply `performance` to issues that describe a regression or improvement
related to speed, memory, or resource usage. Apply `security` to issues
that describe a security vulnerability, hardening task, or compliance
requirement. These are deliberately grouped together because they often
require specialized review and measurement.

---

Following the guidelines above keeps the issue tracker visually
organized, makes triage predictable, and ensures that automation
workflows (such as the issue-automation workflow) can act on labels
reliably. If you are unsure which label to use, prefer the more
specific label and ask a maintainer in a comment if clarification is
needed.
