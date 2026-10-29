# Claude in VS Code

Many of us write code, LaTeX and notes in **Visual Studio Code**. The **Claude Code extension** puts Claude in a panel inside VS Code, where it can read your project, propose changes as diffs you accept or reject, and run commands. It works with your Pro account; no API key needed.

## Install

1. Open VS Code (version 1.94 or later).
2. Open the Extensions view: `Cmd+Shift+X` (Mac) or `Ctrl+Shift+X` (Windows/Linux).
3. Search for **Claude Code** (publisher: Anthropic) and click **Install**.
4. Click the **spark icon** that appears at the top right of an open file, or in the left Activity Bar.
5. Sign in with your **Claude Pro** account when asked.

If the icon does not appear, run **Developer: Reload Window** from the Command Palette (`Cmd/Ctrl+Shift+P`).

## Open your project the right way

Claude works on the **folder you open** in VS Code. Open the folder of your paper, course or analysis (**File → Open Folder**), not a single file. Claude can then read everything in it, and only that.

## Everyday use

| You want to… | Do this |
|---|---|
| Ask about a piece of code | Select the lines. Claude sees the selection automatically. Then ask *"What does this do?"* |
| Point Claude to a file | Type `@` and the file name: *"Compare `@fit_spectrum.py` with `@fit_spectrum_old.py`"*. `Option+K` / `Alt+K` inserts the current selection as a reference. |
| Have Claude change code | Describe the change. Claude shows each edit as a **diff**; accept or reject it. |
| Plan before changing anything | Type `/plan` followed by the task. Claude proposes a plan you can edit before it touches any file. |
| Work on several things | Open several conversations in separate tabs. |
| Think harder | Raise the **effort** level (from the `/` menu) for tricky bugs and derivations. |

## Not just code

VS Code + Claude is also a good way to work on **LaTeX papers, lecture notes and Markdown**:

- *"Fix all LaTeX warnings in `main.tex` and make the citation style consistent."*
- *"Read my `% TODO` comments in `chapter3.tex` and address each one."*
- *"Turn `notes.md` into a structured outline for section 2 of the paper."*

See the worked examples: [Write a conference proceeding](../examples/research/conference-proceeding.md) and [Lecture notes from slides](../examples/teaching/lecture-notes-from-slides.md).

## Tell Claude about your project

Put a `CLAUDE.md` file at the top of the folder: what the project is, how to run it, conventions, what not to touch. Claude reads it at the start of every conversation. Type `/init` to have Claude draft one. More in [Claude Code](claude-code.md#make-it-know-your-project).

## Stay in control

- **Use git** (VS Code has it built in, in the Source Control panel). Commit before a big change so you can undo it.
- **Read the diffs** before accepting. Claude can be confidently wrong.
- **Permission mode**: Claude now starts in **Auto**, where a safety classifier reviews most actions instead of asking you. While you learn, click the mode indicator at the bottom of the prompt box and pick **Manual**, which asks before each change.
- Don't open folders that contain secrets or data you are not allowed to share. See [Data and privacy](../getting-started/data-and-privacy.md).

## Extension or terminal?

The extension and the terminal version (`claude` in a terminal, see [Claude Code](claude-code.md)) are the same assistant. The extension is easier if you already live in VS Code; the terminal works everywhere, including over SSH on a cluster. Your conversations are shared between them.

Reference: [Claude Code in VS Code](https://code.claude.com/docs/en/vs-code) (Anthropic documentation).
