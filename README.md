# Noise, Light and Heat: A Multi-Stressor Synthesis of Urban Effects on Avian Vocal Behaviour

**Zoology Research Assistant Internship — Week 3** | Rabi Narayan Patra | 12 October 2026

A **collaborative virtual research synthesis**: five independently developed research components, each written
to a role brief as though by a separate member of a research team, integrated into one coherent paper with
explicit handovers, transition arguments and a claim-by-claim audit.

## The scientific contribution

The synthesis answers a question no single component could. Because traffic noise, artificial light and the
urban heat island all rise together with urban intensity, single-stressor studies estimate each effect partly
confounded with the others. Entering all three in the same model isolates them — and the result is that **each
stressor owns a different target**:

| Response | Dominant stressor | Unique R² |
|---|---|---|
| **The signal** — minimum song frequency | noise — **+4.68 Hz per dB** (95% CI 4.22–5.14, p < 0.001) | 0.0022 |
| **The timing** — dawn-song onset | light — **−0.429 min per unit radiance** (CI −0.490 to −0.367) | 0.1489 |
| **The effort** — vocal activity rate | heat — **−0.188 songs/min per °C** (CI −0.215 to −0.161) | 0.1162 |

Noise does nothing measurable to timing or effort; light does nothing to frequency or effort; heat does nothing
to frequency. The three are **separable, not redundant**.

## The largest effect is the least-studied stressor

Heat's effect on vocal activity is the largest single effect in the study, and thermal stress has the thinnest
behavioural literature of the three. Across the observed range of heat island intensity it implies a reduction
of about a quarter of the mean activity rate.

## A negative result converted into a design specification

Neither interaction term is estimable at 24 cities. Rather than report that and move on, the quantitative
component ran a power analysis — correctly using the **between-city** residual variance (0.75 min), not the
recording-level residual (5.08 min), which would have made power appear flat at every city count:

| Cities | Power (noise × light) |
|---|---|
| 24 (this study) | 14% |
| 100 | 61% |
| **200** | **85%** |
| 300 | 95% |

Detecting an interaction between two site-level stressors needs **~200 cities**. The null is a limit on what the
study could detect, not evidence of independence.

## How the collaboration is made auditable

- **Role briefs** — each component states what it must produce and what it hands on
- **Handover markers** — every section names what it inherited and what it passes on
- **Transition paragraphs** — the integrator's explicit bridges between components
- **Integration audit** (Section 6) — a table tracing all 13 claims to the component that produced them
- **One real disagreement** reported rather than smoothed over: the acoustic analyst's exclusion rule vs the
  quantitative analyst's preference, and why retention won

## Repository contents

```
├── README.md
├── Collaborative_Research_Synthesis.docx    # the paper (22 pages, ~6,550 words)
├── Collaborative_Research_Synthesis.pdf
├── key_results.md                           # the estimates and the power table
└── data_dictionary.csv                      # every variable, its role and its definition
```

**In the v1.0 release bundle:** the extended dataset, the generative ground truth, all outputs, the six figures,
and the full simulation/analysis/figure/report code.

## Reproducing it

```bash
python3 scripts/01_extend_dataset.py   # adds the heat dimension and the new response
python3 scripts/02_analysis.py         # multi-stressor models, power analysis, robustness
python3 scripts/03_make_figures.py     # all six figures
python3 scripts/04_build_report.py     # assembles the paper
```

## Author

**Rabi Narayan Patra** — Zoology Research Assistant Intern, 2026.
GitHub: [@rabinarayanpatra350-biotech](https://github.com/rabinarayanpatra350-biotech)
