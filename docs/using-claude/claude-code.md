# Claude Code

Claude Code is Claude working directly on your computer, inside a code folder. It reads your files, edits them, runs commands and tests, and uses git. It is included in Pro and shares the same usage allowance as chat.

Use it instead of the chat when the task is about **your own code**: a pipeline, an analysis repository, a simulation, a LaTeX paper.

## Where to run it

- **Terminal** (macOS, Linux, Windows): the full version. Instructions below.
- **VS Code** and **JetBrains**: install the Claude Code extension. It shows changes as diffs in the editor. See [Claude in VS Code](vs-code.md).
- **Desktop app**: open the **Code** tab. No separate install; you see diffs visually, run several sessions side by side and can schedule recurring tasks.
- **Web** ([claude.ai/code](https://claude.ai/code)) and the **mobile app**: no install. These work on a GitHub repository in the cloud, not on your laptop, and keep running when you close the page.
- **Remote Control**: start a session on your own machine, then follow and steer it from your phone or another browser.

## Install (terminal)

macOS, Linux or WSL:

```bash
curl -fsSL https://claude.ai/install.sh | bash
```

Windows PowerShell:

```powershell
irm https://claude.ai/install.ps1 | iex
```

Or with Homebrew (`brew install --cask claude-code`) or WinGet (`winget install Anthropic.ClaudeCode`); these two don't update automatically. Check it worked with `claude --version` in a new terminal window.

Then go to a project folder and start it:

```bash
cd ~/work/my-analysis
claude
```

The first time, it opens your browser to log in. Choose your **Claude Pro** account.

Full and up-to-date instructions: [Claude Code quickstart](https://code.claude.com/docs/en/quickstart).

## Good first tasks

Start by letting it read before it writes:

- *"What does this project do? Explain the folder structure."*
- *"Where is the redshift-space distortion computed, and what are its inputs?"*

Then small, checkable changes:

- *"Write tests for `cosmology.py`, then run them."*
- *"This script crashes with the attached error. Find and fix the cause."*
- *"Convert this Fortran 77 routine to Python with numpy, and check both give the same output on the test file."*
- *"Fix the LaTeX warnings in `paper.tex` and make the reference style consistent."*
- *"Review my uncommitted changes and point out bugs."*

## Stay in control

- **Use git.** Commit before asking for big changes, so you can always go back. Ask Claude to *"show me what you changed"* before you commit.
- **Permissions.** On Pro, Claude Code now starts in **Auto** mode: a safety classifier reviews most actions instead of asking you. Press `Shift+Tab` to switch mode, for example to **Manual** (asks before every change) while you learn, or to **plan mode** to get a plan before anything is touched. Typing `/plan` followed by a task does the same.
- **Don't run it on folders with secrets or data you cannot share** (see [Data and privacy](../getting-started/data-and-privacy.md)). It reads what it needs from the folder you start it in.
- **Check the results**: run the tests and look at the plots. Claude Code can be confidently wrong about scientific details.

## Make it know your project

Create a file called `CLAUDE.md` at the top of your repository. Claude Code reads it at the start of every session. Put in it what a new student would need to know:

```markdown
# Project notes for Claude
- Python 3.11, numpy/scipy/astropy. Run tests with `pytest tests/`.
- Units: distances in Mpc/h, masses in Msun/h.
- Never modify files in `data/raw/`.
- The main pipeline entry point is `run_pipeline.py`.
```

Type `/init` in Claude Code to have it draft one for you. Claude Code also keeps its own **auto memory** of what it learns about the project between sessions.

## Go further

- **Skills**: type `/` to see the commands and skills available. You can write your own (for example, "how we produce paper figures") and Claude Code uses them when relevant. See [Skills](tasks.md#skills).
- **Scheduled tasks**: `/schedule` creates a task that runs in the cloud on a schedule, such as a nightly test run or a weekly dependency check.
- **One-off commands**: `claude -p "explain this function"` answers and exits, so you can use Claude in scripts.
- **Connect tools** with MCP servers, for example to read issues from GitLab or tickets from a tracker.

## Useful commands

| Command | What it does |
|---|---|
| `claude` | Start a session in the current folder |
| `claude -c` | Continue the last session in this folder |
| `claude -r` | Pick an earlier session to resume |
| `/clear` | Start a fresh conversation (use it when you change task) |
| `/help` | List commands |
| `Shift+Tab` | Switch permission mode |
| `Esc` | Interrupt Claude |

To learn more, the free [Claude Code 101](https://academy.claude.com/courses/claude-code-101) course is a good next step.
