# Data Engineering Fundamentals

<div align="center">

**Think like a data engineer by lunch.**

*The only DE course where every concept is a live simulator — not a slide, not a video.*

[![Live Demo](https://img.shields.io/badge/Live_Demo-Open_Course-%2306B6D4?style=for-the-badge)](https://www.timloehr.me/de-fundamentals/)
[![GitHub Stars](https://img.shields.io/github/stars/Mavengence/data-engineering-fundamentals?style=for-the-badge&color=FDEE21)](https://github.com/Mavengence/data-engineering-fundamentals/stargazers)
[![License: MIT](https://img.shields.io/badge/License-MIT-white?style=for-the-badge)](LICENSE)

</div>

---

<!--
  📸 ADD A DEMO GIF HERE — this is the #1 thing that drives stars.
  Record 30 seconds:
    1. Hover pipeline dots on the Overview → detail cards appear
    2. Ch0: flip Scanner from row to columnar → 99 columns vanish, one glows blue
    3. Ch3: drag skew slider to 90% → worker 0 overflows with OVERLOADED label
    4. Ch9: click a sabotage button → rows burst at the gate
  Tools: Cleanshot X, QuickTime + gifski, Kap, or Loom.
  Target: < 5 MB, 800px wide, 15 fps.
-->

## What this is

A browser-native crash course on building production data pipelines.
10 chapters. 15 live simulators. No slides. No video. No account.

The course treats every concept as a **failure mode** — you learn what watermarks are
by watching events drop when you drag the wrong window. You learn what key skew is by
cranking a slider until worker 0 overflows. You learn what idempotency means by watching
a retry double-count every row in real time.

**By the end you know where a pipeline fails before it does.**

---

## Try it now — no install

```
https://www.timloehr.me/de-fundamentals/
```

Or run it locally in 30 seconds:

```bash
git clone https://github.com/Mavengence/data-engineering-fundamentals.git
cd data-engineering-fundamentals
python3 .serve.py          # → http://127.0.0.1:5002
```

No npm. No build step. Open `index.html` directly in Chrome and it also works.

---

## What makes this different

| Most DE resources | This course |
|---|---|
| 9-week bootcamp with homework | ~90 minutes, self-paced |
| Explains tools (Kafka, Spark, dbt) | Explains the *problems* that made those tools necessary |
| Videos you watch passively | Simulators you break on purpose |
| Correct output, no failure modes | Every concept taught through its failure mode |
| Requires a cloud account or Docker | Runs entirely in your browser |

---

## The 10 chapters

| # | Chapter | The lesson in one line |
|---|---------|----------------------|
| 00 | Core Fundamentals | Why columnar skips 99% of disk — and what Parquet actually is |
| 01 | Ingest | Two clocks per event. The wrong one decides what you lose. |
| 02 | Streaming | Fast loses on completeness; slow loses on latency. Pick one. |
| 03 | Store | One bad day on Day 3 poisons every day that follows it. |
| 04 | Compute | The planner bets on statistics. Wrong stats, wrong plan. |
| 05 | Orchestrate | A task that ran twice must equal a task that ran once. Non-negotiable. |
| 06 | Quality | A bad row is worse than a missing row — the bad one ships to the exec deck. |
| 07 | Discover | Six commands. The answer in under 3 seconds. Always. |
| 08 | Serve | Five teams. Five DAU numbers. One meeting. |
| 09 | Govern | An unannotated PII column never ships. |
| 10 | Capstone | Break any one of six contracts. Watch exactly what fails downstream. |

---

## The 15 simulators

Every concept has a live sim. Here are the best ones:

**Column scanner** — flip row to columnar. 99 columns dim to near-invisible; the target
column glows blue. The progress bar covers 100x more ground. You feel the 100x speedup
before you read the explanation.

**Watermark drag** — drag the event-time window left and right. Events turn amber and
drop as your window closes. The late-event problem becomes physical.

**Hash-join shuffle** — drag key skew to 90%. Worker 0 overflows with a pulsing
OVERLOADED banner. The other workers dim to near-empty. You see the hot-key problem
in your peripheral vision.

**Idempotent backfill** — flip INSERT OVERWRITE to INSERT. Introduce a failure. Watch
the retry double-count every row. Flip back. Problem gone.

**Guided Capstone** — six contracts, six sabotage buttons. Hit "guided tutorial" and
watch 48 seconds of automated chaos: each contract breaks in turn, rows burst at the
gate, the downstream number goes wrong. Then everything restores.

*Plus:* byte latency trace, 7-layer stack, SQL planner, streaming conveyor, cumulative
table scrubber, trust meter, discovery speedrun, lineage camera, metrics query, and
permission gate.

---

## Tech

Vanilla React 18 via CDN · Babel standalone · plain CSS · no bundler · no npm install.

The whole course is a single `index.html` that loads chapter files from `src/chapters/`.
Fork it. Teach with it. Embed it in your own onboarding.

```
data-engineering-fundamentals/
├── index.html              ← entry point, loads everything
├── styles.css              ← all styles (~3,700 lines)
├── lib/theme-tokens.css    ← design tokens
├── src/chapters/           ← one JSX file per chapter
│   ├── App.jsx             ← sidebar + routing
│   ├── shared.jsx          ← Hero, Panel, Takeaway, Callout components
│   ├── Ch_Overview.jsx     ← animated pipeline overview
│   ├── Ch0_Fundamentals.jsx
│   ├── Ch0_StackSims.jsx   ← LayerCake, ByteTrace, SqlDecoder, ConnectorSwitcher
│   ├── Ch1_Ingest.jsx
│   ├── Ch1_5_Streaming.jsx ← the big conveyor belt sim
│   └── ...                 ← Ch2 through Ch9
└── .serve.py               ← no-cache dev server
```

---

## Contributing

Found a wrong number? A sim that does not teach clearly? Open an issue or a PR.

Each chapter is a single self-contained JSX file. You can read any of them top-to-bottom
in under 10 minutes. Adding a new simulator means adding a React component to the
relevant chapter file — no build pipeline to fight.

---

## License

MIT — fork it, teach with it, build on it.

---

<div align="center">

If this helped you think differently about data pipelines, a star helps others find it.

**[Open the course](https://www.timloehr.me/de-fundamentals/)** · **[Star on GitHub](https://github.com/Mavengence/data-engineering-fundamentals)**

</div>
