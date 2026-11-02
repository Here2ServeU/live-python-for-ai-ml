# Python for AI-ML · Free Live Sessions

Data in, prediction out, summary back: Python that runs anywhere and tells the truth.

**Free · Live · 30 minutes · Mondays and Thursdays, 7:30 PM Central** · with Emmanuel N. ([Transformed 2 Succeed](https://transformed2succeed.com))

### [Register free on Zoom](https://us06web.zoom.us/meeting/register/fT235rLjQaihJYrWj2_vjw)

Register once and you're in for every session. Zoom emails you the join link and reminders. Bring your questions: every session ends with live Q&A.

## Watch the recordings

Missed a session or want to watch it again? Recordings are added here after each live session.

| Date | Recording |
|---|---|
| _Coming after the first session_ | |

## Set up your lab (do this before you join)

Want to code along? Follow **[SETUP.md](SETUP.md)**. It takes about 15 minutes, once, and works on any computer (or right in your browser with GitHub Codespaces).

## Downloads

Everything you need is in the [`downloads`](downloads) folder:

| File | What it is |
|---|---|
| [02_Python_for_AI_ML_Free_Live_Session.pdf](downloads/02_Python_for_AI_ML_Free_Live_Session.pdf) | The session slides (PDF) |
| [02_Python_for_AI_ML_SETUP_GUIDE.pdf](downloads/02_Python_for_AI_ML_SETUP_GUIDE.pdf) | The setup guide (PDF version of SETUP.md) |
| [python-for-ai-ml-repo.zip](downloads/python-for-ai-ml-repo.zip) | The lab files (unzip, then follow SETUP.md) |


## What you'll learn

1. **Python That Runs Anywhere**: Box it. Pin it. Rebuild it. Inspect a real dataset with plain Python.
2. **A Model You Can Trust**: Don't trust the Desert Forecaster. Train two fraud models and score them fairly.
3. **Make It Explain Itself**: Check the meter. Get a plain-English summary from an AI, with its cost.

## Three things to remember

- **Box it. Pin it. Rebuild it.**: Module 1. venv, freeze, install -r: a stranger can rebuild and run your project.
- **Don't trust the Desert Forecaster**: Module 2. On rare events, 97% accuracy can mean zero fraud caught. F1 can't be fooled.
- **Check the meter.**: Module 3. Input and output tokens, priced separately, logged on every call.

## Try it yourself

To get the lab files, download **[python-for-ai-ml-repo.zip](downloads/python-for-ai-ml-repo.zip)** from the downloads folder (see [SETUP.md](SETUP.md)).

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

## All free live sessions

A different course every session. The rotation repeats every 4 weeks, so if you miss one, it comes back around.

| Week | Day | Course |
|---|---|---|
| Week 1 | Monday | [Linux for AI-ML Systems](https://github.com/Here2ServeU/live-linux-for-ai-ml) |
| Week 1 | Thursday | **Python for AI-ML** (you are here) |
| Week 2 | Monday | [Zero to AI-ML Systems Engineering](https://github.com/Here2ServeU/live-zero-to-ai-ml) |
| Week 2 | Thursday | [DevOps for AI-ML Systems](https://github.com/Here2ServeU/live-devops-for-ai-ml) |
| Week 3 | Monday | [SRE for AI-ML Systems](https://github.com/Here2ServeU/live-sre-for-ai-ml) |
| Week 3 | Thursday | [GPU Optimization for AI-ML Systems](https://github.com/Here2ServeU/live-gpu-optimization-for-ai-ml) |
| Week 4 | Monday | [FinOps for AI-ML Systems](https://github.com/Here2ServeU/live-finops-for-ai-ml) |
| Week 4 | Thursday | [AI Agent Operations](https://github.com/Here2ServeU/live-ai-agent-operations) |

## Want the full course?

The membership gives you **all 8 courses, every module and every lab, for $49/month**, plus a live session every month where we build something together.

**[Join at transformed2succeed.com](https://transformed2succeed.com)**
