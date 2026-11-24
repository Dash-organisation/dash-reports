# CLAUDE.md — dash-reports

DASH-01: a 6-DoF biped. This repo is the **read-only mirror** of the reports: HTML galleries, Léo-Paul's
write-ups, videos, heavy experiment data and raw sim-to-real logs. The code and the live report workspace are in
`dash-sim2real`. Human docs: `README.md`. Write docs and commit messages in English.

## Layout

- `report/` — report workspace mirrored from `dash-sim2real/report/` (galleries `*-videos.html`, `*.md`, `figures/`, `data/`).
- `docs/experiments/` — complete experiment records, heavy files included.
- `RLframework/results/` — results read by the galleries.
- `sim2real-logs/` — raw black-box data of the hardware runs (`.bbseg`, `.bbdump`, CSV, NPZ) and `ANALYSE.md` files (French).

## Rules

- **Content comes from `dash-sim2real` only**, through `tools/sync_reports.sh [--push]` run from a dash-sim2real
  clone. Do not edit `report/`, `docs/experiments/` or `RLframework/results/` here: edit them in dash-sim2real and sync.
- **Never move or rename files**: the galleries link to these paths and `report/manifest.json` hashes the bytes
  (`python report/scripts/build_report.py --frozen`). Do not reformat, re-encode or change line endings
  (`.gitattributes` keeps `report/**` and `docs/experiments/**` as `-text`).
- Nothing is ever deleted here (the sync never deletes): ask before removing any file.
- Edits made directly here are limited to `README.md`, `LICENSE`, `.gitattributes` and this Claude setup.
- No Git LFS. Keep every file under 25 MB; GitHub refuses files over 100 MB.
- Theses, midterm presentations and `report/presentations/` are not published: never add them.

## Workflow

- The sync script commits on `main` (`report: sync from dash-sim2real@<sha> (<branch>)`). Other changes: a
  `docs/<topic>` branch and a pull request. Commit messages: `area: what changes`.
- Ask before `git push`; never force-push (history is large, ~900 MB).
- `../dash-sim2real` and `../dash-cad` are separate repos: do not edit, switch branches or commit in them from here.

## Saving tokens

This repo is mostly data. Do not open: `**/*.mp4`, `**/*.png`, `**/*.pdf`, `**/*.npz`, `**/*.pkl`, `**/*.msgpack`,
`**/*.jsonl`, `**/*.csv`, `*.bbseg`, `*.bbdump`, `report/manifest.json`, `report/data/**`. Use `head`, `jq`, `wc`
or a short Python one-liner on what you need. For a series, start from the gallery table in `README.md` and the
matching `report/*.md`.
