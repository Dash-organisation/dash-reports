# AGENTS.md — dash-reports

Instructions for AI coding assistants (Codex, Cursor, Copilot, ChatGPT, …). Claude Code reads `CLAUDE.md`; the
rules there apply to every assistant, so read it first.

## The essentials (full version in CLAUDE.md)

- Read-only mirror of `dash-sim2real/report/`, `docs/experiments/` and `RLframework/results/`, filled by
  `tools/sync_reports.sh` from dash-sim2real. Do not edit those folders here.
- Never move, rename, reformat or delete files: the galleries and `report/manifest.json` depend on exact paths and bytes.
- Do not open videos, images, NPZ, JSONL, CSV or black-box logs whole.
- Non-sync changes on a `docs/<topic>` branch with a pull request. Ask before `git push`; never force-push.
