# DevOps Activity Log Site

Welcome to the DevOps Pages lab repository. This project publishes a GitHub Pages
site that automatically renders your latest GitHub activity on the homepage.

- **Site URL:** configure via GitHub Pages → Settings → Pages (branch `main`, folder `/`).
- **Workflow:** `.github/workflows/activity-log.yml` gathers recent events and updates the section below.
- **Secret required:** `TOKEN` (PAT with `public_repo`; add `repo` if private activity is needed).

## Latest Activity
<!-- ACTIVITY-LOG:START -->

<!-- ACTIVITY-LOG:END -->

## How It Works

1. GitHub Actions checks out this repository.
2. The workflow queries recent public events for your username with the PAT stored in `TOKEN`.
3. The script rewrites the activity section between the markers above.
4. `stefanzweifel/git-auto-commit-action` commits the update with a bot-style message.
5. `index.md` includes this README so the published page reflects the latest activity automatically.

## Local Development

```sh
npm install --global @githubnext/github-pages && github-pages --help
```

The site is pure Markdown/HTML, so any static site preview tool works. GitHub Pages builds the markdown
using Jekyll’s default settings—no extra configuration required.

## Repository Tasks Checklist

- [ ] Push this repository to GitHub.
- [ ] Add the `TOKEN` secret (Settings → Secrets and variables → Actions).
- [ ] Enable GitHub Pages (Settings → Pages → Build and deployment → Branch: `main`, Folder: `/`).
- [ ] Trigger `Pages` build (`git push` or Actions → `Run workflow`).
- [ ] Confirm the live URL renders the README content.
- [ ] Capture screenshots and workflow links for the final report.

## Report Template

The file `report-template.md` outlines a 6–10 page structure for the required PDF deliverable.
Fill it in with screenshots, links, and reflections, then export to PDF for submission.

