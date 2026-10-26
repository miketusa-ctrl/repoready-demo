# RepoReady Lite by Harlo

5 CI-verified, SHA-pinned GitHub Actions workflows + repo hygiene. MIT licensed.

| File | What it does | Secrets / setup |
|---|---|---|
| `.github/workflows/ci-node.yml` | Node.js test matrix | none |
| `.github/workflows/ci-python.yml` | Python test matrix | none |
| `.github/workflows/ci-go.yml` | Go test matrix | none |
| `.github/workflows/release-on-tag.yml` | GitHub Release on v* tag | none (uses GITHUB_TOKEN, contents: write) |
| `.github/workflows/stale.yml` | Mark/close stale issues and PRs | none |

No-project-file safe: Node/Go jobs skip gracefully when `package.json`/`go.mod` is absent; Python falls back to `unittest`.

## Install
Copy the `.github/` folder (and `SECURITY.md`, `CONTRIBUTING.md`) into your repo root, commit, push. Workflows run on next push/PR.

## Customize
- Versions: edit the `matrix` lists (Node/Python/Go).
- Branch: replace `main` under `on.push.branches`.
- Every action is pinned to a full commit SHA with the version tag in a trailing comment; Dependabot (`.github/dependabot.yml`, weekly npm/pip/gomod/github-actions) keeps pins fresh.
- Hygiene: issue forms (`.github/ISSUE_TEMPLATE/`), `PULL_REQUEST_TEMPLATE.md`, `SECURITY.md`, `CONTRIBUTING.md`.

Support: digitalpromohub.support@gmail.com

## Want more?
**RepoReady Pro** (24 workflows: CodeQL, Pages deploy, Dependabot auto-merge, changelog, labeler, Docker publish, lint suites, link/license/secret checks...) and **Team** license — coming soon on Gumroad (https://gumroad.com).


> Demo repo for CI evidence (Harlo / RepoReady). Not the public Lite funnel.
