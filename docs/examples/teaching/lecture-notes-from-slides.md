---
tags:
  - Teaching
  - Claude Code
  - VS Code
  - LaTeX
---

# Turn your slides into lecture notes, chapter by chapter

!!! info "Illustrative example"
    This example was written by the site editors to show the workflow. It is not yet a real ICCUB experience. If you try it, [send us your version](../../contribute/index.md) and we will replace it.

| About this example | |
| --- | --- |
| **Author** | ICCUB Claude Guide editors |
| **Date** | 2026-10-06 |
| **Area** | Teaching (any course) |
| **Tools used** | Claude Code in VS Code, LaTeX |
| **Time saved** | Several weeks over a semester (estimate) |

## Goal

Students ask for written notes, but the course only has slides. Turn 12 lectures of slides into proper LaTeX lecture notes with text, worked examples and figures, while keeping full control of the content.

## What I did

### 1. Prepare the folder

```text
course-notes/
├── CLAUDE.md
├── slides/          ← lecture01.pdf … lecture12.pdf
├── extra/           ← syllabus, past exams, your handwritten derivations
└── notes/           ← empty: Claude will create the LaTeX here
```

`CLAUDE.md` says who the students are, the language, the notation, and the rules:

```markdown
# Lecture notes: Introduction to Cosmology (3rd year, Grau en Física)
- Language: English. Level: students know mechanics, electromagnetism, basic GR is NOT assumed.
- One chapter per lecture, in notes/chapters/chNN.tex, included from notes/main.tex.
- Follow the order and content of the slides; don't add topics that aren't in the slides
  unless I ask.
- Each chapter: learning goals, text, at least one worked example, a short summary,
  three exercises (no solutions in the main text).
- Figures: redraw simple plots with TikZ/pgfplots; for complex ones, insert
  \missingfigure{description} and I will provide them.
- References: only textbooks listed in extra/syllabus.pdf.
```

### 2. Build the template first

> *Create notes/main.tex as a book-style document with a title page, table of contents, a chapter per lecture (empty for now), a consistent theorem/example/exercise environment, and our notation macros. Compile it.*

Check the PDF and fix the layout now; every chapter will inherit it.

### 3. Go chapter by chapter

> *Write chapter 1 from slides/lecture01.pdf following CLAUDE.md. Compile and stop.*

Read the PDF of the chapter. Then open `ch01.tex` and **review it by writing comments directly in the file**, where the problem is:

```latex
% CLAUDE: add a worked example here: age of an Einstein–de Sitter universe with H0 = 70
% CLAUDE: this figure doesn't look good, make the axes logarithmic and label both curves
% CLAUDE: add a reference to Ryden ch. 5 for the derivation
% CLAUDE: remove this paragraph, too advanced for 3rd year
```

Then:

> *Address all `% CLAUDE:` comments in ch01.tex, remove them when done, compile, and summarise what you changed.*

Repeat until the chapter is right, then move to the next one. Later chapters go faster, because you can say *"same structure and level as chapter 1"*.

### 4. Final pass

> *Check notation consistency across all chapters, make sure every exercise is numbered and referenced, and build a list of all `\missingfigure` placeholders.*

## Result

A full set of compiled lecture notes, consistent in notation and style, with worked examples and exercises, built at the pace of one chapter per week alongside the course.

## What to watch for

- **Physics errors**: check every derivation and worked example. Factors of 2 and sign conventions are where errors hide.
- **Content creep**: without the "don't add topics" rule, notes grow beyond what you teach.
- **Figures**: TikZ redraws are good for simple plots; check axes and labels. Don't copy figures from textbooks without permission.
- **Commit after each chapter** so you can go back.
- If you share the notes, say they were prepared with AI assistance.
