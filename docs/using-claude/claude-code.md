# Claude Code

Claude Code is Claude working directly on your computer, inside a code folder. It reads your files, edits them, runs commands and tests, and uses git. It is included in Pro and shares the same usage allowance as chat.

Use it instead of the chat when the task is about **your own code**: a pipeline, an analysis repository, a simulation, a LaTeX paper.

!!! tip "Most researchers: use the desktop app"
    The easiest way to use Claude Code is the **Code** tab of the Claude desktop app. No terminal, nothing else to install: you pick a folder, describe what you want, and review the changes on screen. The rest of this page assumes the desktop app; the [terminal version](#terminal-version) is at the end.

## Where to run it

- **Desktop app** (macOS, Windows, Linux beta): the **Code** tab. Recommended. Instructions below.
- **VS Code** and **JetBrains**: install the Claude Code extension. It shows changes as diffs in the editor. See [Claude in VS Code](vs-code.md).
- **Terminal**: the `claude` command. Useful on a cluster over SSH or if you already work in a terminal. See [Terminal version](#terminal-version).
- **Web** ([claude.ai/code](https://claude.ai/code)): works on a GitHub repository in the cloud, not on your laptop.

All of them are the same assistant, with the same `CLAUDE.md` and settings.

## Install the desktop app

1. Download Claude for your system:
    - **macOS** (Intel and Apple Silicon): [download](https://claude.ai/api/desktop/darwin/universal/dmg/latest/redirect)
    - **Windows** (x64): [download](https://claude.ai/api/desktop/win32/x64/setup/latest/redirect). For ARM laptops: [ARM64 installer](https://claude.ai/api/desktop/win32/arm64/setup/latest/redirect)
    - **Linux** (beta, Ubuntu/Debian): see [Claude Desktop on Linux](https://code.claude.com/docs/en/desktop-linux)

    All downloads are also on [claude.com/download](https://claude.com/download).

2. Install and open Claude, then sign in with your **Claude Pro** account.
3. Click the **Code** tab at the top center. (The other tabs are **Chat**, the normal conversation, and **Cowork**, for longer tasks that run in the background.)

The app already contains Claude Code: you do not need Node.js or the terminal version.

## Your first session

1. **Choose where it runs.** Select **Local** to work on files on your computer, then click **Select folder** and pick your project folder. Start with a small project you know well.
2. **Choose a model** in the dropdown next to the send button.
3. **Choose a permission mode** in the selector next to the send button. While you learn, pick **Manual**: Claude asks before editing a file or running a command.
4. **Describe the task** in the prompt box, as you would in the chat. See [Good first tasks](#good-first-tasks).
5. **Review the changes.** In **Manual** mode, each change appears as a diff with **Accept** and **Reject** buttons. In the other modes, Claude applies its edits and an indicator like `+12 -1` appears: click it to see every change file by file. You can comment on a specific line and Claude will revise.

You do not have to wait for Claude to finish: click the stop button to interrupt it, or type a correction and press **Enter** to redirect it while it works.

### Permission modes

| Mode | What Claude does |
|---|---|
| **Manual** | Asks before editing files or running commands. Best to start. |
| **Accept edits** | Edits files without asking, still asks before commands. |
| **Plan** | Only proposes a plan, changes nothing. Good before a big change. |
| **Auto** | Works without asking; risky actions are blocked automatically. |

### Useful things in the Code tab

- **Add context**: type `@` and a file name to point Claude at a file, or drag in PDFs, images and plots.
- **Terminal**: press `` Ctrl+` `` to open a terminal in the project folder, to run things yourself.
- **Several tasks at once**: **+ New session** in the sidebar. Each session has its own conversation and folder.
- **Side question**: press `Cmd+;` (macOS) or `Ctrl+;` (Windows) to ask something without disturbing the main task.
- **Commands and skills**: type `/` in the prompt box, for example `/init` (see [below](#make-it-know-your-project)) or `/code-review`.
- **Remote machines**: instead of **Local**, choose **SSH** to work on a server or cluster where you have an account, or **Cloud** to run a long task that continues when you close the app.
- **Git**: not required for a simple session, but strongly recommended (see [Stay in control](#stay-in-control)). Some features, such as running each session in its own worktree, need it. On Windows, install [Git for Windows](https://git-scm.com/downloads/win).

Full reference: [Claude Code desktop documentation](https://code.claude.com/docs/en/desktop) and the [desktop quickstart](https://code.claude.com/docs/en/desktop-quickstart).

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

- **Use git.** Commit before asking for big changes, so you can always go back. Review the diff (or ask Claude to *"show me what you changed"*) before you commit.
- **Permissions.** Depending on the permission mode, Claude Code may run commands and edit files without asking each time. Start in **Manual** and switch only once you trust the task.
- **Don't run it on folders with secrets or data you cannot share** (see [Data and privacy](../getting-started/data-and-privacy.md)). It reads what it needs from the folder you open.
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

Type `/init` in Claude Code to have it draft one for you.

## Terminal version

The same Claude Code also runs as the `claude` command in a terminal. It is handy on a cluster over SSH, or if you prefer the command line.

macOS, Linux or WSL:

```bash
curl -fsSL https://claude.ai/install.sh | bash
```

Windows PowerShell:

```powershell
irm https://claude.ai/install.ps1 | iex
```

Or with Homebrew: `brew install --cask claude-code`. Check it worked with `claude --version`.

Then go to a project folder and start it:

```bash
cd ~/work/my-analysis
claude
```

The first time, it opens your browser to log in. Choose your **Claude Pro** account. Press `Shift+Tab` to switch permission mode.

| Command | What it does |
|---|---|
| `claude` | Start a session in the current folder |
| `claude -c` | Continue the last session in this folder |
| `/clear` | Start a fresh conversation (use it when you change task) |
| `/help` | List commands |
| `Esc` | Interrupt Claude |

Full instructions: [Claude Code quickstart](https://code.claude.com/docs/en/quickstart).

To learn more, the free [Claude Code 101](https://academy.claude.com/courses/claude-code-101) course is a good next step.
