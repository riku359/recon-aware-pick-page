# Reconstruction-Aware Cryo-EM Particle Picking — Project Page

Local static project page for **Reconstruction-Aware Cryo-EM Particle Picking**.
Manuscript sources: `~/Desktop/wacv2027`.
Built in the same style as `~/CryoAnomaly-page`.

Open:

- `index.html`

## Assets

Rendered from `~/Desktop/wacv2027/figures/pdf/` with `pdftoppm -png`:

| file | paper figure |
|---|---|
| `assets/pipeline_overview.png` | Fig. 1 (`fig:pipeline`) — the pipeline and its feedback loop |
| `assets/locres_maps_10081_10532.jpg` | Fig. 3 (`fig:maps`) — local-resolution maps on EMPIAR-10081 / 10532 |
| `assets/pick_fates.jpg` | Fig. 2 (`fig:pick_fates`) — what survives each stage |
| `assets/f1_vs_resolution.png` | Fig. 4 (`fig:f1_vs_res`) — 2D F1 against reconstruction resolution |
| `assets/cryosift_scores.png` | Fig. 5 (`fig:cryosift_scores`) — the 2D selection failure on EMPIAR-10345 |
| `assets/cleaner_failure.jpg` | Fig. 6 (`fig:cleaner_failure`) — the mask failure on EMPIAR-10532 |

Re-render any of them with:

```bash
pdftoppm -png -r 240 -singlefile \
    ~/Desktop/wacv2027/figures/pdf/<name>.pdf assets/<name>
```

Tables on the page, and where they come from in the manuscript:

| page section | manuscript table |
|---|---|
| Main Results | `tab:main_results` (`sec/5_results.tex`) |
| Ablation Study | `tab:ablation_res` + `tab:particles`, merged into one table with row groups (`sec/5_results.tex`) |

Deliberately left off the page: `tab:datasets` (`sec/4_experiments.tex`, along with the
whole Experimental Setup section), `tab:mask_removals`, `tab:loop_rounds` and
`tab:teacher_quality` (`sec/5_results.tex`, along with the whole Feedback Loop section),
`tab:f1_vs_res` (`supp.tex` §S7), and `tab:cryosegnet_purified` (`sec/6_discussion.tex`).
The Failure Cases section (`fig:cryosift_scores`, `fig:cleaner_failure`) was removed too.

The page carries almost no running prose by design: what is left is the abstract, the
three contribution cards, and the figure captions.

## Dummies to replace before public release

- **Teaser video** — the teaser slot is a placeholder box. Drop the real file at
  `assets/teaser_video.mp4`, then delete the `.video-placeholder` div in the teaser
  section of `index.html` and uncomment the `<video>` block right above it.
- **Links** — arXiv / Paper / Supplementary / Code are all `href="#"` (styled gray via
  `.button.dummy`). Fill in the real URLs and drop the `dummy` class.
- **BibTeX** — placeholder entry with `booktitle = {TBD}`.

## Note

The page names the authors while the paper is still under review. Keep it unpublished
(or drop the author block) until the decision is out.
