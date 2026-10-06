---
tags:
  - Research
  - Claude Code
  - VS Code
  - LaTeX
---

# Write a paper draft from a project folder

!!! info "Illustrative example"
    This example was written by the site editors to show the workflow. It is not yet a real ICCUB experience. If you try it, [send us your version](../../contribute/index.md) and we will replace it.

| About this example | |
| --- | --- |
| **Author** | ICCUB Claude Guide editors |
| **Date** | 2026-10-06 |
| **Area** | Any |
| **Tools used** | Claude Code in VS Code, LaTeX, git |
| **Time saved** | First full draft in an afternoon instead of one to two weeks (estimate) |

## Goal

Turn a finished analysis (notes, calculations, figures, a results table) into a complete first draft of a paper in the journal's LaTeX format, written in our own style, that we then revise ourselves.

## What I did

### 1. Put everything in one folder

```text
paper-cluster-lensing/
├── CLAUDE.md            ← instructions for Claude (step 2)
├── notes/               ← meeting notes, logbook, emails pasted as text
├── calculations/        ← derivations (LaTeX or scanned + transcribed), notebooks
├── figures/             ← final PDF figures
├── results/             ← tables of fitted parameters (CSV)
├── refs/                ← key papers (PDF) and refs.bib
└── paper/               ← journal template (e.g. aa.cls / mnras.cls), empty main.tex
```

Make it a git repository (`git init`, then commit) so every change Claude makes can be reviewed and undone.

### 2. Write clear instructions in `CLAUDE.md`

This is the most important step. Claude reads it at the start of every session.

```markdown
# Paper: Weak-lensing masses of 40 galaxy clusters

## Target
- Journal: A&A, using paper/aa.cls. About 12 pages.
- Audience: cluster cosmology community.

## Content
- Main result: mass–richness relation, slope 1.08 ± 0.06 (results/fit_summary.csv).
- Sections: Introduction, Data, Method, Results, Systematics, Discussion, Conclusions.
- Method is described in notes/method.md and calculations/shear_profile.tex.

## Style
- Plain, precise English. Short paragraphs. "We", active voice.
- Use the notation of calculations/shear_profile.tex.
- Every number must come from a file in results/ or a figure. Never invent numbers.

## References
- Only cite entries that exist in refs/refs.bib. If a citation is needed that is
  not there, write \cite{TODO:description} and list it at the end.

## Workflow
- Write one section at a time and stop for review.
- Never edit files outside paper/.
```

### 3. Open the folder in VS Code and start

Open the folder (**File → Open Folder**), open the Claude panel (spark icon), and start with planning, not writing:

> */plan Read CLAUDE.md, the notes, calculations and results. Propose a detailed outline of the paper: for each section, the key points, which figures and tables go where, and which references. Don't write any LaTeX yet.*

Correct the outline in the chat until it matches what you want.

### 4. Write section by section

> *Write the Data section in paper/main.tex following the agreed outline. Then stop.*

Read the diff, accept, compile, and read the PDF. Then the next section. For the Results section:

> *Write the Results section. Take every number from results/fit_summary.csv and say in a LaTeX comment next to each number which file and column it came from.*

### 5. Review by leaving comments in the file

Instead of explaining changes in the chat, write them directly in `main.tex` as comments, then ask Claude to address them:

```latex
% CLAUDE: too long, cut this paragraph to three sentences
% CLAUDE: add a sentence comparing with the X-ray masses (refs: Mantz2016)
% CLAUDE: this contradicts Table 2, check
```

> *Address every `% CLAUDE:` comment in main.tex, remove each comment once done, and list what you changed.*

### 6. Final checks

> *Check that every \ref and \cite resolves, every figure is referenced in the text, and every number in the text matches results/. List anything that doesn't.*

## Result

A compiled, complete first draft with figures, tables and bibliography, in our notation, in the journal format. The text needed real revision (see below) but the structure and most paragraphs were usable.

## What to watch for

- **Numbers**: check every number against your results files, even with the "never invent" instruction.
- **References**: Claude can attribute a claim to the wrong paper. Check each citation says what the text claims.
- **Overclaiming**: drafts tend to sound more certain than the results justify. Tone down the abstract and conclusions yourself.
- **Your voice**: the paper must remain yours. Rewrite the introduction and discussion yourself; they are where the scientific judgement is.
- **Collaboration rules and journal policy**: check that your collaboration allows uploading internal material, and declare AI assistance as the journal requires. See [Data and privacy](../../getting-started/data-and-privacy.md).
