# Launch copy

Ready-to-use text for each distribution channel. Post these in order:
HN first (Tuesday–Thursday 8–10 AM ET), then cross-post the others.

---

## Show HN

**Title:**
```
Show HN: Data engineering concepts as live simulators — drag the watermark, overflow a worker, break a pipeline gate
```

**First comment (post this immediately after submitting):**
```
I built this course while working as a data engineer at Meta for new-hire onboarding.
After running it internally, I sanitized and open-sourced it.

The premise: every DE concept is better learned through its failure mode than through
its happy path. So instead of explaining what a watermark is, there is a simulator
where you drag the window and watch late events disappear. Instead of explaining key
skew, you drag a slider until one worker overflows and the others go idle.

Ten chapters, fifteen simulators, runs entirely in your browser.
No signup, no npm install, no cloud account.

Happy to answer questions about any of the sims or the pedagogy behind them.
```

---

## r/dataengineering

**Title:**
```
I open-sourced the DE fundamentals course I built at Meta for new-hire onboarding
```

**Body:**
```
Every concept is a live simulator. You drag the watermark and watch events drop.
You push key skew to 90% and watch one worker overflow while the others idle.
You flip INSERT OVERWRITE to INSERT, introduce a failure, and watch the retry
double-count every row.

10 chapters, 15 simulators, runs in the browser with no install.

GitHub: https://github.com/Mavengence/data-engineering-fundamentals
Live: https://www.timloehr.me/data-engineering-fundamentals/
```

---

## LinkedIn

```
I built an internal data engineering course at Meta for new-hire onboarding.
Last week I open-sourced it.

Every concept is a live simulator:
- Drag the watermark window. Events disappear silently when it is set wrong.
- Push key skew to 90%. One worker overflows, the rest go idle.
- Flip INSERT OVERWRITE to INSERT. A retry doubles every row in real time.
- Break any of six pipeline contracts in the Capstone. Watch exactly what fails downstream.

10 chapters. 15 simulators. Runs in your browser. No install, no account.

https://github.com/Mavengence/data-engineering-fundamentals
```

---

## Awesome list PR body

For igorbarinov/awesome-data-engineering and similar repos:

```
Adding Data Engineering Fundamentals, an interactive browser-based course covering
10 DE concepts through live simulators (watermark drag, hash-join shuffle,
idempotent backfill, trust meter, capstone pipeline). No install required.
```

---

## Submission targets (in order of impact)

1. Show HN — highest quality traffic, highest star conversion
2. r/dataengineering — large audience, directly relevant
3. PR to igorbarinov/awesome-data-engineering
4. PR to DataTalksClub/data-engineering-zoomcamp (they maintain an awesome-data-engineering.md)
5. LinkedIn (German market via loehrning.ai audience)
6. DataTalks.Club Slack #shameless-self-promotion
7. r/learnprogramming
8. r/Python (the .serve.py angle — "a Python-served interactive course")

---

## Custom social preview image

GitHub shows a 1280x640px image when this URL is shared on Twitter/LinkedIn.
Upload `assets/social-preview.png` (create a screenshot of the pipeline overview
at 1280x640) at:
Settings > General > Social preview > Upload an image.

This doubles click-through rate from social shares.
