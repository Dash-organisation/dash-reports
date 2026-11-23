# dash-reports

Reports, galleries, videos and heavy data of the DASH-01 project. The code is in [`dash-sim2real`](https://github.com/Dash-organisation/dash-sim2real).

The `report/`, `docs/experiments/` and `RLframework/results/` paths are **the same as in the old repo** (DASH-01@3574ddd). The HTML galleries point into these three folders, and `python report/scripts/build_report.py --frozen` checks the file hashes, so do not move them.

## Galleries by series

Open the `.html` files from a local clone, in the browser. The entries link to `dash-sim2real/docs/rl/EXPERIMENTS.md`.

| Series | Gallery | Entry |
| --- | --- | --- |
| STOP-01 to 06 | [`report/index.html`](report/index.html) | [STOP-01 to 06](https://github.com/Dash-organisation/dash-sim2real/blob/main/docs/rl/EXPERIMENTS.md#stop-01-to-06) |
| Transfer of Nathann's policy to CAD-v2 | [`report/policy-transfer01-videos.html`](report/policy-transfer01-videos.html) | — |
| GAIT-04 to 11 | [04](report/gait04-videos.html), [06](report/gait06-videos.html), [07](report/gait07-videos.html), [08](report/gait08-videos.html), [09](report/gait09-videos.html), [11](report/gait11-videos.html), [flat-feet](report/flatfeet-videos.html) | [GAIT-01 to 11](https://github.com/Dash-organisation/dash-sim2real/blob/main/docs/rl/EXPERIMENTS.md#gait-01-to-11) |
| WALK-01 | [videos](report/walk01-videos.html), [CPU previews](report/walk01-cpu-previews.html), [diagnostics](report/walk01-diagnostics.html) | [SPEED-01, WALK-01](https://github.com/Dash-organisation/dash-sim2real/blob/main/docs/rl/EXPERIMENTS.md#speed-01-walk-01) |
| CLEARANCE-01/02 | [01](report/clearance01-videos.html), [02](report/clearance02-videos.html) | [CLEARANCE-01/02](https://github.com/Dash-organisation/dash-sim2real/blob/main/docs/rl/EXPERIMENTS.md#clearance-0102) |
| STAND-03 | [`report/standing03-videos.html`](report/standing03-videos.html) | [STAND-03](https://github.com/Dash-organisation/dash-sim2real/blob/main/docs/rl/EXPERIMENTS.md#stand-03) |
| STAND-04 (deployed policy) | [`report/standing04-videos.html`](report/standing04-videos.html) | [STAND-04](https://github.com/Dash-organisation/dash-sim2real/blob/main/docs/rl/EXPERIMENTS.md#stand-04) |
| QUIET-01v2 | [`report/quiet01v2-videos.html`](report/quiet01v2-videos.html) | [QUIET-01 v1, v2](https://github.com/Dash-organisation/dash-sim2real/blob/main/docs/rl/EXPERIMENTS.md#quiet-01-v1-v2) |
| QUIET-PUSH-01 | [`report/quiet-push01-videos.html`](report/quiet-push01-videos.html) | [QUIET-PUSH-01](https://github.com/Dash-organisation/dash-sim2real/blob/main/docs/rl/EXPERIMENTS.md#quiet-push-01) |

Léo-Paul's write-ups are in `report/*.md`; [`report/README.md`](report/README.md) is the entry point.

## Other folders

| Folder | Contents |
| --- | --- |
| `docs/experiments/` | complete experiment records, including files over 1 MB (`progress.csv`…). Files under 1 MB are also in `dash-sim2real` |
| `RLframework/results/` | results read by the galleries |
| `sim2real-logs/` | raw black-box data of runs 3 to 9 (2026-11-17 to 11-20) and the plan C benches: `.bbseg`, `.bbdump`, CSV, JSON, NPZ. The `ANALYSE.md` analyses (in French) are also in `dash-sim2real/docs/sim2real/Logs/`, with English summaries in `dash-sim2real/docs/sim2real/README.md` |

This is a plain git repo, **without LFS**. No file is larger than 25 MB. We will move to LFS if the repo grows past 2 to 3 GB.

## What is not published

The theses, the midterm presentations and Léo-Paul's `report/presentations/midterm-2026-10-29/` folder are not in this repo. The `report/scripts/*midterm*` scripts and `update_final_challenges.py` read that folder, so they do not work without it.

## License

[Mozilla Public License 2.0](LICENSE), the same as the old DASH-01 repo.
