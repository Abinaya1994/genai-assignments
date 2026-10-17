# GitHub Code Review Dashboard --- Human Prompt Master Roadmap 🚀

> **For AI Trainers & Learners**: This document provides a
> phase-by-phase prompt roadmap to build a custom **GitHub Code Review
> Dashboard** in the existing workspace. Each prompt is written from a
> human user's perspective so it can be copied into GitHub Copilot or
> another AI coding assistant. The AI coding assistant is responsible
> for inspecting the existing project, creating the required files,
> implementing the code, and validating the result.

------------------------------------------------------------------------

## 📌 How to Use This Roadmap

1.  Save this file in the root of your workspace as
    `GITHUB_CODE_REVIEW_ROADMAP.md`.
2.  Open the workspace in GitHub Copilot and ask it to read this file
    completely.
3.  Follow each phase sequentially from Phase 1 to Phase 6.
4.  Copy the prompt inside **"📋 Copy-Paste Prompt for AI Assistant"**
    and paste it into Copilot Chat.
5.  Let Copilot inspect the current project and implement the phase's
    actual code, not just describe a solution.
6.  Run the **"🧪 User-Facing Verification Steps"** before moving to the
    next phase.
7.  If a check fails, ask Copilot to fix the issue and rerun the
    relevant checks before proceeding.
8.  Do not expose secrets or tokens in frontend code, source control,
    screenshots, or logs.
9.  If the workspace already has a framework or working components,
    preserve and reuse them instead of replacing them without a reason.
10. The dashboard must clearly distinguish live GitHub data from
    mock/sample data.

------------------------------------------------------------------------

## Global Requirements for Every Phase

-   Build a custom UI for reviewing GitHub pull requests and monitoring
    code-review activity.
-   Inspect the current workspace before choosing or changing
    technologies. Reuse the existing stack whenever practical.
-   Implement real, connected behavior wherever the required integration
    and credentials are available. Do not stop at static mockups or
    pseudocode.
-   Create or modify the necessary source files, styles, configuration,
    tests, and documentation for each phase.
-   Keep implementation modular, readable, maintainable, responsive, and
    accessible.
-   Use the official Bank of America logo only when an approved asset is
    supplied or available through an authorized source. Preserve its
    original proportions and do not redraw or distort it.
-   Use the Bank of America organization name and approved brand assets
    only in accordance with the organization's brand-use rules. Do not
    imply official endorsement unless authorized.
-   Suggested brand-inspired starting tokens: red `#E31837`, deep navy
    `#012169`, white `#FFFFFF`, light neutral `#F3F5F7`, and dark
    neutral text `#374151`. Treat these as proposed design tokens, not
    confirmation of the complete official brand palette; verify against
    approved brand guidelines before production.
-   Use red and navy for brand accents, navigation, and primary actions.
    Use accessible semantic colors for success, warning, and failure
    states, with text or icons as well as color.
-   Keep GitHub credentials, webhook secrets, and privileged operations
    on the server side.
-   Validate GitHub webhook signatures before accepting event payloads.
    Handle duplicate delivery IDs safely.
-   Do not invent live metrics, successful test results, existing files,
    or connected services.
-   When external access is unavailable, use clearly labeled mock data
    for UI development and explain exactly what remains to be
    configured.
-   At the end of every phase, report files created or modified,
    functionality implemented, commands actually run, test outcomes,
    unresolved issues, and the next phase.
-   Do not claim a phase is complete unless its verification steps have
    been checked. Fix failures before moving on.

------------------------------------------------------------------------

## Phase 1: Creating the Application & Visual Design System

### 🎯 Phase Goal

Build the initial visual foundation for an enterprise GitHub Code Review
Dashboard. Establish a clean, modern Bank of America brand-aligned
visual system with consistent colors, typography, layout, responsive
behavior, and reusable UI elements.

### 📋 Copy-Paste Prompt for AI Assistant

``` text
Read this roadmap completely and start with Phase 1 only.

Inspect my existing workspace before creating or modifying files. Identify the frontend framework, application entry point, styling approach, existing components, available scripts, and current backend or webhook integration. Reuse the existing stack and preserve working functionality.

Build the visual foundation for a custom application called "GitHub Code Review Dashboard".

Create a polished enterprise interface with a white and light-neutral content area, deep navy navigation elements, and controlled red accents inspired by Bank of America branding. Use the proposed color tokens in this roadmap as starting values and keep them centralized so they can be updated to match approved brand guidelines.

Create consistent typography, spacing, buttons, inputs, cards, tables, status badges, borders, focus states, and responsive breakpoints. Use a subtle professional background rather than distracting animations. Ensure text is readable, controls have visible focus states, and the layout works on desktop, tablet, and mobile.

Prepare the main application shell and reusable styling/components needed by later phases. Do not hard-code real GitHub metrics. If a placeholder is needed, label it clearly as sample data.

Generate the actual source files and working code. Do not provide only a design description or pseudocode. Run the existing build, lint, and type-check commands where available, fix errors introduced by the changes, and report the exact files created or modified and the actual validation results.

Do not begin Phase 2 until Phase 1 is implemented and verified.
```

### 🧪 User-Facing Verification Steps

-   [ ] Open the application in a browser and confirm that it loads
    without a blank screen.
-   [ ] **Theme Check**: Verify that the interface uses a consistent
    white/light-neutral content area, deep navy, and red accents.
-   [ ] **Component Check**: Confirm that buttons, cards, inputs,
    tables, and status badges share consistent styling.
-   [ ] **Responsive Check**: Resize the browser to desktop, tablet, and
    mobile widths.
-   [ ] **Accessibility Check**: Navigate with the keyboard and verify
    that focus indicators are visible.
-   [ ] **Build Check**: Confirm the project's available build and lint
    checks pass, or document pre-existing failures separately.

------------------------------------------------------------------------

## Phase 2: Building the Sticky Header, Organization Branding & Navigation

### 🎯 Phase Goal

Add a clear application header with the approved Bank of America logo
and organization name, dashboard title, GitHub connection status,
navigation links, and a responsive navigation layout.

### 📋 Copy-Paste Prompt for AI Assistant

``` text
Implement Phase 2 of GITHUB_CODE_REVIEW_ROADMAP.md. Inspect the Phase 1 implementation and reuse its design system.

Add a professional header for the "GitHub Code Review Dashboard".

Place the approved Bank of America logo at the top-left of the header, followed by the organization name or approved brand lockup and the product title "GitHub Code Review Dashboard". Use only an approved logo asset supplied in the workspace or an authorized asset source. Preserve the asset's original aspect ratio, clear space, and colors. If no approved asset is available, create a clearly labeled logo placeholder and tell me where the approved asset should be placed; do not fabricate the logo.

Add navigation items for:
- Overview
- Pull Requests
- Review Analytics
- Repositories
- Webhook Events
- Settings or API/Integration Status, as appropriate to the existing application

Show a GitHub connection status indicator with distinct Connected, Disconnected, and Error states. Do not display "Connected" unless the backend has verified the connection. When the integration is not configured, show "Not configured" rather than pretending it is connected.

Make the header sticky if appropriate for the existing layout. Use the established navy, red, white, and neutral tokens. Keep the header uncluttered, ensure navigation has a clear active state, and make it responsive on smaller screens.

Wire navigation to actual routes or functional views where the project supports them. Do not leave controls that appear interactive but do nothing. Create the actual code, run available checks, and report the files changed and validation results. Do not begin Phase 3 until Phase 2 is verified.
```

### 🧪 User-Facing Verification Steps

-   [ ] **Logo Check**: Confirm the approved logo is placed at the
    top-left and is not stretched or distorted.
-   [ ] **Brand Name Check**: Verify the organization name and dashboard
    title are legible and correctly aligned.
-   [ ] **Navigation Check**: Select each navigation item and confirm it
    opens the corresponding view or clearly indicates that the view is
    not yet implemented.
-   [ ] **Connection Status Check**: Verify the status reflects the real
    integration state or displays "Not configured".
-   [ ] **Sticky Header Check**: Scroll the page and confirm the header
    remains usable.
-   [ ] **Mobile Check**: Confirm the header and navigation fit smaller
    screens.

------------------------------------------------------------------------

## Phase 3: Building the Dashboard Overview, Metrics Cards & Pull Request Table

### 🎯 Phase Goal

Create the main dashboard with summary metrics, review trends, filters,
and a pull-request list that makes pending work and review risks easy to
identify.

### 📋 Copy-Paste Prompt for AI Assistant

``` text
Implement Phase 3 of GITHUB_CODE_REVIEW_ROADMAP.md. Reuse the existing application shell and design system.

Create the main "Code Review Overview" page.

At the top, add a filter row with:
- Repository selector
- Pull-request state selector
- Author or reviewer selector where supported by the available data
- Date-range selector
- Search by pull-request number or title
- Clear-filters action

Add summary metric cards for:
- Open pull requests
- Pull requests awaiting review
- Pull requests with changes requested
- Pull requests merged in the selected period
- Median time to first review
- Median time to merge

Add trend charts for review turnaround and pull-request activity when sufficient data is available. Use a charting library already present in the project; introduce a dependency only if justified and documented.

Create a pull-request table with columns for pull-request number, title, repository, author, assigned reviewers, current state, review status, CI/check status where available, age, and last update. Include sorting, pagination, empty states, loading states, error states, and links to the corresponding GitHub pull request.

Make old or blocked pull requests easy to identify using configurable thresholds. Use accessible labels and text alongside status colors.

All metric cards, charts, and rows must use the same filters and reporting period. Define metric formulas and exclusions clearly. Do not invent values or claim that a pull request is overdue unless the threshold is configured. If the GitHub integration is not connected, display labeled sample data or a clear setup state.

Implement the actual UI and data interfaces. Connect to existing APIs if available; otherwise, define the interface needed for the backend phase without pretending the data is live. Add tests for filtering and metric presentation where possible. Run available checks and report actual results before proceeding.
```

### 🧪 User-Facing Verification Steps

-   [ ] **Metric Check**: Confirm all summary cards display values or a
    clear unavailable/loading state.
-   [ ] **Filter Check**: Change repository, status, and date filters;
    verify the displayed table and metrics respond consistently.
-   [ ] **Search Check**: Search by pull-request number or title and
    verify matching rows are shown.
-   [ ] **Table Check**: Verify sorting, pagination, status indicators,
    and GitHub links.
-   [ ] **Trend Check**: Confirm charts display the selected reporting
    period and do not imply missing data is zero.
-   [ ] **Sample Data Check**: Verify any mock data is clearly labeled.

------------------------------------------------------------------------

## Phase 4: Designing the Pull Request Review Workspace & Detailed Review Information

### 🎯 Phase Goal

Create a detailed review workspace for an individual pull request,
showing review activity, reviewer decisions, comments, code-change
summaries, CI results, and security findings when available.

### 📋 Copy-Paste Prompt for AI Assistant

``` text
Implement Phase 4 of GITHUB_CODE_REVIEW_ROADMAP.md.

Create a detailed pull-request review workspace that opens when a user selects a pull request from the dashboard.

Display the following information when provided by GitHub or connected integrations:
- Pull-request title, number, repository, author, and link
- Description and current state
- Creation, update, review, and merge timestamps
- Assigned reviewers and their review status
- Approval, changes-requested, and pending-review counts
- Review comments and review activity timeline
- Changed-file count, additions, and deletions
- CI/check-run results
- Linked security findings and severity, if a supported source provides them
- Relevant labels, branches, and linked issues when available

Use clear sections or tabs such as Overview, Reviews & Comments, Changes Summary, Checks, and Activity. Provide direct links to GitHub for detailed code diffs and actions that the dashboard does not implement.

Add loading, empty, permission-denied, not-found, and connection-error states. Make timestamps and timezones clear. Do not display private repository details to users who are not authorized to view them.

If AI-generated review summaries or recommendations are part of the existing system, label them as AI-generated and keep them separate from actual GitHub review decisions. Do not invent reviewer approvals, comments, CI results, or security findings.

Generate and integrate the actual code, add appropriate tests, and validate navigation and error states. Report the files changed and the actual test results before moving to Phase 5.
```

### 🧪 User-Facing Verification Steps

-   [ ] **Detail Navigation Check**: Open a pull request from the
    overview table and verify the correct details are shown.
-   [ ] **Review Check**: Verify approvals, change requests, pending
    reviews, and comments match the available source data.
-   [ ] **Activity Check**: Confirm events appear in a meaningful
    timeline with appropriate timestamps.
-   [ ] **CI Check**: Verify check-run status is shown only when the
    source provides it.
-   [ ] **Security Check**: Confirm unavailable security data is labeled
    appropriately and access restrictions are respected.
-   [ ] **Error Check**: Test loading, not-found, permission-denied, and
    disconnected states.

------------------------------------------------------------------------

## Phase 5: GitHub Webhook Connection, Event Processing & Error Handling

### 🎯 Phase Goal

Connect the dashboard to GitHub through secure webhooks and the existing
framework, including n8n where applicable. Process relevant events,
update dashboard data, and provide transparent integration health and
error handling.

### 📋 Copy-Paste Prompt for AI Assistant

``` text
Implement Phase 5 of GITHUB_CODE_REVIEW_ROADMAP.md. First inspect the existing backend, webhook routes, n8n workflows, environment configuration, and integration patterns. Reuse working components.

Connect the dashboard to GitHub through a secure backend webhook endpoint. Support the event types needed for the dashboard, including relevant pull_request, pull_request_review, pull_request_review_comment, pull_request_review_thread where supported, push, and check_run or check_suite events.

Implement the following behavior:
1. Receive GitHub webhook requests through the configured endpoint.
2. Validate the X-Hub-Signature-256 header using the configured webhook secret and a timing-safe signature comparison before processing the event.
3. Validate required headers and payload structure.
4. Check repository authorization and accept only supported event types.
5. Record the GitHub delivery identifier and process duplicate deliveries idempotently.
6. Normalize incoming events into the application's internal data model.
7. Persist events and update the relevant pull-request and repository records when a database is configured.
8. Handle retries, transient failures, delayed events, and out-of-order event arrival safely.
9. Update the dashboard through the existing API or an appropriate refresh mechanism.
10. Expose integration health, last successful event time, processing failures, and safe diagnostic information.
11. Use the existing n8n workflow when it is part of the current architecture. Keep signature validation and sensitive authorization logic in a trusted backend layer unless the existing implementation provides an equally secure verified approach.
12. Keep all webhook secrets and GitHub credentials on the server side.

Send a clear, safe error response for invalid signatures, malformed payloads, unauthorized repositories, unsupported events, and temporary failures. Avoid logging secrets or unnecessary sensitive payload content.

Provide an environment-variable template with placeholder values only. Document required GitHub webhook settings, callback URL, selected event types, permissions, and setup steps. Never fabricate a successful live connection.

Create automated tests for valid signatures, invalid signatures, duplicate delivery IDs, malformed payloads, unsupported events, retry behavior, and event processing. Use representative fixture payloads when real GitHub credentials are unavailable and label those tests accordingly.

Implement actual code and workflow changes, run available tests, and report exactly what is working and what still requires external configuration.
```

### 🧪 User-Facing Verification Steps

-   [ ] **Configuration Check**: Verify the webhook URL and required
    environment variables are documented.
-   [ ] **Signature Check**: Confirm valid signed events are accepted
    and invalid signatures are rejected.
-   [ ] **Event Check**: Send a representative pull-request or review
    event and verify it is normalized and processed.
-   [ ] **Duplicate Check**: Replay the same delivery ID and verify
    duplicate effects are prevented.
-   [ ] **Dashboard Refresh Check**: Verify an accepted event updates
    the appropriate data after processing.
-   [ ] **Error Handling Check**: Confirm malformed payloads and
    processing failures produce safe, useful diagnostics.
-   [ ] **Secret Check**: Confirm tokens and webhook secrets are not
    present in frontend bundles, browser network responses, source
    control, or logs.

------------------------------------------------------------------------

## Phase 6: Review Analytics, Results Presentation, Testing & Operational Readiness

### 🎯 Phase Goal

Complete the dashboard with review analytics, historical trends, clear
result formatting, robust states, and end-to-end verification so the
application is ready for controlled deployment.

### 📋 Copy-Paste Prompt for AI Assistant

``` text
Implement Phase 6 of GITHUB_CODE_REVIEW_ROADMAP.md and complete the remaining integration and quality work.

Add an analytics area that presents the available code-review metrics over selectable date ranges and repositories.

Include:
- Pull-request volume and merge trends
- Open-review backlog and backlog aging
- Median and average time to first review
- Median and average time to merge
- Approval and changes-requested trends using a documented denominator
- Review activity by repository, team, or reviewer when supported by the available data
- CI/check failures when provided by GitHub
- Security finding counts and severity only when supplied by a supported integration
- A list of pull requests that need attention based on configurable thresholds

Document each metric's formula, time window, exclusions, data source, and treatment of missing values. Ensure filters are applied consistently across cards, charts, and tables.

Improve the result presentation with readable chart labels, formatted timestamps, clear status badges, responsive tables, accessible tooltips, and helpful loading, empty, stale-data, and error states. If the dashboard includes an AI-generated review summary, render its structured output safely and clearly distinguish it from verified GitHub data.

Complete end-to-end validation across the user journey:
1. Open the dashboard.
2. Check the GitHub integration status.
3. Filter repositories and pull requests.
4. Open a pull-request detail view.
5. Review comments, approvals, checks, and activity where available.
6. Process a webhook event.
7. Verify that the appropriate dashboard data is updated.
8. Test invalid signatures, duplicate events, missing permissions, and temporary integration failures.

Run the existing build, lint, type-check, unit, integration, and end-to-end checks where available. Add missing tests appropriate to the existing framework. Review authentication, authorization, dependency security, accessibility, responsive layouts, logging, and error handling.

Provide setup, deployment, monitoring, troubleshooting, backup/recovery, and rollback instructions appropriate to the actual project. Do not claim production readiness if critical tests are failing or required security controls are missing.

At completion, report:
- Files created and modified
- Features implemented
- Architecture and data flow
- GitHub and n8n configuration required
- Commands executed and actual results
- Tests passed, failed, skipped, or blocked
- Security and accessibility findings
- Known limitations and remaining work
- Deployment and rollback steps

Do not claim that a build, test, webhook, integration, or deployment succeeded unless it was actually verified.
```

### 🧪 User-Facing Verification Steps

-   [ ] **Analytics Check**: Verify charts and metrics use documented
    formulas and selected filters.
-   [ ] **Historical Data Check**: Confirm the reporting period and
    missing-data behavior are clear.
-   [ ] **End-to-End Check**: Complete the
    dashboard-to-pull-request-to-webhook workflow.
-   [ ] **Failure Check**: Verify disconnected integrations and invalid
    events are handled without breaking the UI.
-   [ ] **Security Check**: Confirm credentials remain server-side and
    access controls are enforced.
-   [ ] **Responsive Check**: Validate dashboard tables, charts, and
    details on supported screen sizes.
-   [ ] **Test Report Check**: Review actual test output and ensure
    unresolved critical failures are documented.
-   [ ] **Operational Readiness Check**: Confirm setup, deployment,
    monitoring, and rollback documentation exists.

------------------------------------------------------------------------

## 🎨 Summary of Architecture & Technologies

-   **Frontend Core**: Use the existing framework in the workspace. If
    the project is not yet initialized, propose a maintainable frontend
    stack before implementation.
-   **Design System**: Centralized CSS variables or the existing
    design-token system; responsive layouts; reusable cards, tables,
    charts, navigation, and accessible status indicators.
-   **Branding**: Approved Bank of America logo and brand guidelines;
    proposed red `#E31837`, navy `#012169`, white `#FFFFFF`, light
    neutral `#F3F5F7`, and dark neutral `#374151` tokens pending brand
    verification.
-   **GitHub Integration**: GitHub webhooks and the required GitHub API
    endpoints, with least-privilege permissions.
-   **Backend**: Reuse the existing backend and webhook framework. Do
    not introduce a new backend without first assessing the current
    project.
-   **Automation**: Reuse n8n workflows where they are already part of
    the framework and are appropriate for the processing task.
-   **Persistence**: Use the existing database if available; otherwise,
    document and propose a suitable persistence approach for event
    history and metrics.
-   **Security**: Server-side secret management, webhook signature
    verification, authenticated APIs, authorization, safe logging, and
    idempotent event processing.
-   **Testing**: Use the project's existing test framework for unit,
    integration, end-to-end, accessibility, and security checks.
-   **Deployment**: Follow the existing environment and deployment
    approach. Provide configuration templates, health checks,
    monitoring, troubleshooting, and rollback guidance.

------------------------------------------------------------------------

## 🚀 First Prompt to Start the Project

Copy and paste this into GitHub Copilot Chat after saving this document
in your workspace:

``` text
Read GITHUB_CODE_REVIEW_ROADMAP.md completely and follow its global requirements.

Start with Phase 1 only. Inspect my existing workspace, identify the current frontend and backend stack, application entry points, existing components, GitHub integration, webhook routes, n8n workflows, configuration, and available tests.

Implement the actual Phase 1 code after documenting the current state and implementation plan. Preserve existing working functionality. Run the available validation commands and report the exact files created or modified, the actual results, and any blockers.

Do not start Phase 2 until Phase 1 is implemented and verified. Do not invent live data, credentials, test results, or integrations.
```
