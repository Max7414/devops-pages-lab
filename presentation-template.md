# DevOps Pages Lab Presentation Template and Sample Content

> Recommended slide ratio: 16:9. The outline below is written in Markdown so you can copy it into Google Slides, Keynote, PowerPoint, or any Markdown-to-slides tool.

---

## Template (replace each `TODO` with your content)

### Slide 1 — Cover
- Title: TODO (e.g., DevOps Pages Lab Showcase)
- Name / Student ID: TODO
- Course / Date: TODO

### Slide 2 — Assignment Goals
- TODO: Summarize Part 1 (GitHub Pages publishing)
- TODO: Summarize Part 2 (activity log automation)
- TODO: Optional O-grade enhancements, if delivered

### Slide 3 — Repository & Environment
- TODO: GitHub repository URL
- TODO: Main branch and Pages configuration
- TODO: Tooling or frameworks used (GitHub Actions, Jekyll, etc.)

### Slide 4 — GitHub Pages Setup Flow
- TODO: Step-by-step summary (create repo → push → enable Pages)
- TODO: Add screenshots or flow diagrams (insert inside your slides)
- TODO: Mention blockers and fixes (DNS, build delays, etc.)

### Slide 5 — README and Homepage Integration
- TODO: Explain how `index.md` includes the README content
- TODO: Highlight the README structure and activity block placeholders
- TODO: Call out custom styling or tweaks if any

### Slide 6 — Automation Workflow Overview
- TODO: Summarize `.github/workflows/activity-log.yml`
- TODO: List the Actions used (`checkout`, `github-script`, `git-auto-commit`)
- TODO: Describe schedule vs manual triggers (cron / workflow_dispatch)

### Slide 7 — Token & Security
- TODO: PAT scopes (public_repo vs repo)
- TODO: Secret naming/storage (`TOKEN`)
- TODO: Strategies to prevent leaks (principle of least privilege, rotation)

### Slide 8 — Execution Results
- TODO: Screenshot/snippet of the refreshed README activity section
- TODO: Screenshot or link to a successful Actions run
- TODO: Screenshot of the published Pages homepage

### Slide 9 — Enhancements & Best Practices (Optional for O-grade)
- TODO: Customizations or rationale for scheduling
- TODO: Additional tooling (linting, tests, reporting, etc.)
- TODO: Future improvements or backlog items

### Slide 10 — Takeaways & Q&A
- TODO: Key lessons learned and challenges
- TODO: Next steps or future plans
- TODO: Q&A / contact information

---

## Sample Content (feel free to adapt)

### Slide 1 — Cover
- Title: DevOps Pages Lab Showcase
- Presenter: Max Guo (example)
- Course / Date: DevOps / 2025-10-30

### Slide 2 — Assignment Goals
- Part 1: Publish a static site via GitHub Pages from the `main` branch
- Part 2: Automate GitHub activity collection and render it in the README/homepage
- O-grade: Provide deployment documentation and scheduling rationale for strong repo hygiene

### Slide 3 — Repository & Environment
- Repo: `https://github.com/Max7414/devops-pages-lab`
- Branch & Pages: `main` with “Deploy from a branch / main / root”
- Tooling: GitHub Actions, built-in Jekyll renderer, PAT stored as secret

### Slide 4 — GitHub Pages Setup Flow
- Steps: Initialize locally → push to GitHub → enable Pages → wait for first build
- Tooling: Git CLI, GitHub web console
- Challenges: Initial build delay (~1–2 minutes) solved by refreshing Pages status

### Slide 5 — README and Homepage Integration
- `index.md` uses `{% include_relative README.md %}` to mirror README content
- README reserves `<!-- ACTIVITY-LOG:START/END -->` for workflow updates
- Single-source maintenance: editing README updates both repo and live site

### Slide 6 — Automation Workflow Overview
- Actions: `actions/checkout@v4`, `actions/github-script@v7`, `stefanzweifel/git-auto-commit-action@v5`
- Flow: Fetch user events → format Markdown → replace activity block → auto-commit
- Triggers: Weekday cron (12:00 UTC), push to `main`, manual `workflow_dispatch`

### Slide 7 — Token & Security
- PAT scope: `public_repo` (switch to `repo` for private activity)
- Secret: Stored as `TOKEN`, read inside the workflow with `secrets.TOKEN`
- Safety: Limit scopes, rotate periodically, revoke after course completion

### Slide 8 — Execution Results
- README activity section shows the latest pushes, PRs, and comments
- Actions Run: “Update Activity Log” succeeded on 2025-10-29 (manual trigger)
- Pages URL: `https://max7414.github.io/devops-pages-lab/` displays synced content

### Slide 9 — Enhancements & Best Practices
- Enhancements: Weekday schedule, checklist in README, highlighted workflow steps
- Hygiene: Clean `main` branch, bot-authored commits from automation
- Future work: Add lint/tests, filter events, extend reporting to other repos

### Slide 10 — Takeaways & Q&A
- Takeaways: Learned GitHub Pages + Actions integration and secret management
- Challenges: Debugged `github-script` imports and PAT scope issues
- Next: Expand automation with notifications and richer analytics
- Q&A: Thank you for listening—happy to answer questions!
