# Set up your lab: Python for AI-ML

When you finish, you will have the course project in its own Python "box" (a virtual environment) with every tool installed, and all three module scripts running: inspect the data, train a fraud model, explain it. It takes about 10 minutes, one time.

## What you need

- A Mac, a Windows PC or a Linux computer. You can also use GitHub Codespaces in your browser (needs a free GitHub account).
- **Python 3.11 or newer** (`python3` on Mac and Linux, `py` on Windows).
- A terminal: Terminal on Mac, PowerShell on Windows, or the terminal in VS Code.
- Git, if you want to clone the course repo. VS Code is recommended for reading the scripts, but optional.
- An internet connection for the first install, and about 500 MB of free disk for the tools (pandas, scikit-learn, anthropic).
- **No GPU needed.**
- **No API key needed.** Module 3 runs with `--offline`. An Anthropic API key is optional, only if you want to try one real call later.

## Step 1 · Pick where to run it

### Option A: GitHub Codespaces (easiest, any computer)
1. Sign in to github.com and open this repo.
2. Click **Code > Codespaces > Create codespace on main**.
3. Wait for the terminal at the bottom. Python and git are already installed. Check with `python3 --version`.

### Option B: Windows (PowerShell)
1. Open **PowerShell** and install Python, Git and VS Code (winget ships with Windows 11):
```powershell
winget install Python.Python.3.12
winget install Git.Git
winget install Microsoft.VisualStudioCode
```
2. Close and reopen PowerShell, then check:
```powershell
py --version; git --version
```

### Option C: Mac (Terminal)
1. Install Homebrew first (https://brew.sh), then:
```bash
brew install python git
brew install --cask visual-studio-code
```
2. Check:
```bash
python3 --version && git --version
```

You should see Python 3.11 or newer, and a git version.

## Step 2 · Get the lab files

Download [python-for-ai-ml-repo.zip](downloads/python-for-ai-ml-repo.zip) from the `downloads/` folder of this repo (in Codespaces it is already in `downloads/`). Unzip it and go into the folder.

Mac, Linux or Codespaces (in Codespaces, use `downloads/python-for-ai-ml-repo.zip`):
```bash
unzip python-for-ai-ml-repo.zip
cd python-for-ai-ml
```

Windows (PowerShell, in the folder where the zip is):
```powershell
Expand-Archive python-for-ai-ml-repo.zip -DestinationPath .
cd python-for-ai-ml
```

You should see a `data` folder, a `modules` folder and `requirements.txt`. Run every command from here on inside `python-for-ai-ml`.

## Step 3 · Install and check

Box it (make a virtual environment) and step inside it.

Mac, Linux or Codespaces:
```bash
python3 -m venv .venv
source .venv/bin/activate
```

Windows (PowerShell):
```powershell
py -m venv .venv
.venv\Scripts\Activate.ps1
```

Your prompt now starts with `(.venv)`. Then install the exact tools on the list:

```bash
pip install -r requirements.txt
pip freeze | grep -i pandas
```
(Windows: `pip freeze | findstr pandas`)

You should see some downloading, then `pandas==3.0.5`. Same version as everyone else.

## Step 4 · Quick test for each module

Run these in order, inside `python-for-ai-ml`, with `(.venv)` showing. On Windows, type `py` instead of `python3`.

**Module 1 · Python That Runs Anywhere**
```bash
python3 modules/module-1/scripts/inspect_data.py
```
You should see `rows 5000`, `missing_amount 83`, `fraud_rows 137`, `fraud_rate_pct 2.74`, a fraud rate per merchant, and `saved -> summary.json`.

**Module 2 · A Model You Can Trust**
```bash
python3 modules/module-2/scripts/train.py
```
You should see `3933 train rows · 984 test rows`, three result lines (`random_forest` has accuracy 0.921 and f1 0.381), and `saved -> metrics.json`.

**Module 3 · Make It Explain Itself** (needs Module 2's `metrics.json` first)
```bash
python3 modules/module-3/scripts/explain.py --offline
```
You should see a four-sentence summary that starts `Trust the random forest`, a `usage:` line with `input_tokens=88 output_tokens=77`, and `saved -> summary.md`. `--offline` uses a simulated reply, so no key is needed.

## If something goes wrong

- **`error: data/transactions.csv not found. Are you in the repo root?`** or **`No such file or directory`**: you are in the wrong folder. Run `pwd`; it must end in `python-for-ai-ml`. Then `cd python-for-ai-ml`.
- **`No module named pandas`** (or sklearn): you are outside the box. Activate `.venv` again (Step 3) and check for `(.venv)`.
- **Windows `running scripts is disabled`**: run `Set-ExecutionPolicy -Scope CurrentUser RemoteSigned`, answer `Y`, and activate again. **`py is not recognized`**: close and reopen PowerShell after installing.
- **Mac `brew: command not found`**: install Homebrew first from https://brew.sh.
- **pip cannot find `pandas==3.0.5`**: your Python is older than 3.11. Install a newer Python, delete `.venv`, and repeat Step 3.
- **Module 3 `ANTHROPIC_API_KEY is not set`** or **`No such file or directory: 'metrics.json'`**: add `--offline`, and run Module 2 first.

## Official guides

- Video: Install Git, Python and VS Code on a Mac: https://www.youtube.com/watch?v=8ZIiXg4XOY0&t=6s
- Video: Install Git, Python and VS Code on Windows: https://www.youtube.com/watch?v=f091sbQSv7I
- Python downloads: https://www.python.org/downloads/
- Git downloads: https://git-scm.com/downloads
- Virtual environments (venv): https://docs.python.org/3/library/venv.html
- Homebrew: https://brew.sh
- GitHub Codespaces: https://docs.github.com/codespaces
