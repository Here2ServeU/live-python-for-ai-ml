# Python for AI-ML · Free Live Sessions

Data in, prediction out, summary back: Python that runs anywhere and tells the truth.

Free, live, 30-minute sessions with **Dr. Emmanuel Naweji** ([Transformed 2 Succeed](https://transformed2succeed.com)).
This course is presented on **Week 1, Thursday at 7:30 PM Central** of a 4-week rotation (8 courses, every Monday and Thursday).
This repo holds the slides, the recording of every live session, and the notes and links from each one.

## Session recordings

| Date | Recording | Notes |
|---|---|---|
| _First session coming soon_ | | |
<!-- sessions:end -->

## What the session covers

1. **Python That Runs Anywhere**: Box it. Pin it. Rebuild it. Inspect a real dataset with plain Python.
2. **A Model You Can Trust**: Don't trust the Desert Forecaster. Train two fraud models and score them fairly.
3. **Make It Explain Itself**: Check the meter. Get a plain-English summary from an AI, with its cost.

## Three things to remember

- **Box it. Pin it. Rebuild it.**: Module 1. venv, freeze, install -r: a stranger can rebuild and run your project.
- **Don't trust the Desert Forecaster**: Module 2. On rare events, 97% accuracy can mean zero fraud caught. F1 can't be fooled.
- **Check the meter.**: Module 3. Input and output tokens, priced separately, logged on every call.

## Try it yourself

Clone the course lab repo: [python-for-ai-ml](https://github.com/Here2ServeU/python-for-ai-ml)

**Module 1 · Python That Runs Anywhere**: The commands you'll type in every project

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
pip freeze | grep -i pandas
```
**Module 2 · A Model You Can Trust**: Lab: train both models in one script

```bash
python3 modules/module-2/scripts/train.py
cat metrics.json
```
**Module 3 · Make It Explain Itself**: Lab: run it offline, no key, no cost

```bash
python3 modules/module-3/scripts/explain.py --offline
```

## Slides

[`slides/02_Python_for_AI_ML_Free_Live_Session.pptx`](slides/02_Python_for_AI_ML_Free_Live_Session.pptx): the presenter deck, with full speaker notes.

## Free live session schedule (Mondays and Thursdays, 7:30 PM Central)

| Week | Day | Course |
|---|---|---|
| Week 1 | Monday | [Linux for AI-ML Systems](https://github.com/Here2ServeU/live-linux-for-ai-ml) |
| Week 1 | Thursday | **Python for AI-ML** (this repo) |
| Week 2 | Monday | [Zero to AI-ML Systems Engineering](https://github.com/Here2ServeU/live-zero-to-ai-ml) |
| Week 2 | Thursday | [DevOps for AI-ML Systems](https://github.com/Here2ServeU/live-devops-for-ai-ml) |
| Week 3 | Monday | [SRE for AI-ML Systems](https://github.com/Here2ServeU/live-sre-for-ai-ml) |
| Week 3 | Thursday | [GPU Optimization for AI-ML Systems](https://github.com/Here2ServeU/live-gpu-optimization-for-ai-ml) |
| Week 4 | Monday | [FinOps for AI-ML Systems](https://github.com/Here2ServeU/live-finops-for-ai-ml) |
| Week 4 | Thursday | [AI Agent Operations](https://github.com/Here2ServeU/live-ai-agent-operations) |

## Want all of it?

The membership gives you **all 8 courses, every module and every lab, for $49/month**, plus a live session every month where we build something together.
Join at **https://transformed2succeed.com**.

---

### For the presenter: logging a session

After each live session, run:

```bash
bash scripts/new-session.sh 2026-11-03 "https://link-to-the-recording"
git add -A && git commit -m "Session 2026-11-03" && git push
```

This creates `sessions/2026-11-03.md` from the template (fill in the Q&A and links) and adds a row to the recordings table above.
