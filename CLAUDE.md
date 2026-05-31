# Project notes for Claude

## Workflow
- After creating a PR, squash-merge it yourself. The repo's `auto-merge` GitHub Action is broken and will fail on every PR — ignore that failed check and merge anyway (the GitHub Actions `auto-merge` workflow is unrelated to GitHub's native auto-merge feature; do not enable native auto-merge either).
- **Before deploying a new feature / shipping content** (e.g. a new section, link, project, integration, page), explicitly ask the user whether the AI assistant chatbot needs to know about it. If yes, update the `SYSTEM_PROMPT` in `index.html` (and `candidate.html`) accordingly, or confirm that the DOM auto-grounding + `llms.txt` layers will pick it up. Don't assume.
