# DevOps Activity Log Site

Welcome to the DevOps Pages lab repository. This project publishes a GitHub Pages
site that automatically renders your latest GitHub activity on the homepage.
For a concise overview of the stack and goals, visit the curated [`about.md`](about.md) page.

## Latest Activity
<!-- ACTIVITY-LOG:START -->
- 2025-10-29: Pushed 0 commit(s) to `Max7414/devops-pages-lab@main`
- 2025-10-29: Pushed 0 commit(s) to `Max7414/devops-pages-lab@main`
- 2025-10-29: Created branch main in `Max7414/devops-pages-lab`
- 2025-10-24: Pushed 0 commit(s) to `Max7414/lab6@main`
- 2025-10-24: Pushed 0 commit(s) to `Max7414/lab6@exp3-b`
- 2025-10-24: Pushed 0 commit(s) to `Max7414/lab6@exp3-b`
- 2025-10-24: Public activity in `Max7414/lab6`
- 2025-10-15: Member activity in `jiangyanmu/activity-log`
- 2025-10-08: Pushed 0 commit(s) to `Max7414/activity-log@master`
- 2025-10-08: Pushed 0 commit(s) to `Max7414/activity-log@master`
<!-- ACTIVITY-LOG:END -->

## Repository Highlights

- **Automated feed:** Weekday cron workflow gathers the 10 most recent public GitHub events.
- **Single-source homepage:** `index.md` includes this README so documentation and site stay aligned.
- **Custom styling:** `assets/css/custom.css` provides brand colors, accent blocks, and hero layout.
- **Optional extensions:** Add more markdown pages or adjust the workflow schedule to match course needs.

## Quick Start

1. Create a GitHub repo and push this project (`main` branch).
2. Generate a PAT with `public_repo` scope (or `repo` for private events) and store it as the `TOKEN` secret.
3. Enable GitHub Pages: Settings → Pages → Branch `main`, folder `/`.
4. Run **Update Activity Log** manually the first time to seed the activity block.

## Workflow Summary

```mermaid
flowchart TD
    A[Schedule / Push / Manual Trigger] --> B[actions/checkout@v4]
    B --> C[actions/github-script@v7<br/>fetch user events]
    C --> D{README changed?}
    D -- No --> E[Skip commit]
    D -- Yes --> F[stefanzweifel/git-auto-commit-action@v5]
    F --> G[Activity section updated]
```

## Deliverables Checklist

- [ ] Repo pushed and Pages enabled.
- [ ] `TOKEN` secret configured with valid PAT.
- [ ] README activity section refreshed at least once via workflow.
- [ ] Screenshot of homepage + activity log captured.
- [ ] Workflow run link and bot commit URL saved for the report.
