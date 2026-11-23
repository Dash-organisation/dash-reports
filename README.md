# dash-reports

Rapports, galeries, vidéos et données lourdes du projet DASH-01. Le code est dans [`dash-sim2real`](https://github.com/Dash-organisation/dash-sim2real).

Les chemins `report/`, `docs/experiments/` et `RLframework/results/` sont **les mêmes que dans l'ancien repo** (DASH-01@3574ddd). Les galeries HTML pointent vers ces trois dossiers, et `python report/scripts/build_report.py --frozen` vérifie les empreintes des fichiers. Il ne faut donc pas les déplacer.

## Galeries par série

Ouvrir les `.html` depuis un clone local, dans le navigateur. Les fiches renvoient à `dash-sim2real/docs/rl/EXPERIMENTS.md`.

| Série | Galerie | Fiche |
| --- | --- | --- |
| STOP-01 à 06 | [`report/index.html`](report/index.html) | [STOP-01 à 06](https://github.com/Dash-organisation/dash-sim2real/blob/main/docs/rl/EXPERIMENTS.md#stop-01-à-06) |
| Transfert de la policy de Nathann vers CAD-v2 | [`report/policy-transfer01-videos.html`](report/policy-transfer01-videos.html) | — |
| GAIT-04 à 11 | [04](report/gait04-videos.html), [06](report/gait06-videos.html), [07](report/gait07-videos.html), [08](report/gait08-videos.html), [09](report/gait09-videos.html), [11](report/gait11-videos.html), [flat-feet](report/flatfeet-videos.html) | [GAIT-01 à 11](https://github.com/Dash-organisation/dash-sim2real/blob/main/docs/rl/EXPERIMENTS.md#gait-01-à-11) |
| WALK-01 | [vidéos](report/walk01-videos.html), [aperçus CPU](report/walk01-cpu-previews.html), [diagnostics](report/walk01-diagnostics.html) | [SPEED-01, WALK-01](https://github.com/Dash-organisation/dash-sim2real/blob/main/docs/rl/EXPERIMENTS.md#speed-01-walk-01) |
| CLEARANCE-01/02 | [01](report/clearance01-videos.html), [02](report/clearance02-videos.html) | [CLEARANCE-01/02](https://github.com/Dash-organisation/dash-sim2real/blob/main/docs/rl/EXPERIMENTS.md#clearance-0102) |
| STAND-03 | [`report/standing03-videos.html`](report/standing03-videos.html) | [STAND-03](https://github.com/Dash-organisation/dash-sim2real/blob/main/docs/rl/EXPERIMENTS.md#stand-03) |
| STAND-04 (policy déployée) | [`report/standing04-videos.html`](report/standing04-videos.html) | [STAND-04](https://github.com/Dash-organisation/dash-sim2real/blob/main/docs/rl/EXPERIMENTS.md#stand-04) |

Les textes de Léo-Paul sont dans `report/*.md`. [`report/README.md`](report/README.md) en est le point d'entrée.

## Autres dossiers

| Dossier | Contenu |
| --- | --- |
| `docs/experiments/` | records d'expériences complets, y compris les fichiers de plus de 1 Mo (`progress.csv`…). Les fichiers de moins de 1 Mo sont aussi dans `dash-sim2real` |
| `RLframework/results/` | résultats que lisent les galeries |
| `sim2real-logs/` | données brutes de la black-box des runs 3 à 9 (17–20/11/2026) et bancs du plan C : `.bbseg`, `.bbdump`, CSV, JSON, NPZ. Les analyses `ANALYSE.md` sont aussi dans `dash-sim2real/docs/sim2real/Logs/` |

Le repo est un repo git simple, **sans LFS**. Aucun fichier ne dépasse 25 Mo. On passera à LFS si le repo dépasse 2 à 3 Go.
