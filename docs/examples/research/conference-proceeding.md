---
tags:
  - Research
  - LaTeX
  - Writing
---

# Write a conference proceeding

| About this example | |
| --- | --- |
| **Author** | Vincent Mathieu |
| **Date** | 2026-09-28 |
| **Area** | Hadron physics (theory) |
| **Tools used** | Claude with access to a local project folder |
| **Time saved** | The proceeding was written in about half an hour |
| **Result** | [Meson photoproduction at Jefferson Lab: from two-meson final states to meson-baryon spin-density matrices](https://inspirehep.net/literature/3208903) (INSPIRE) |

## Goal

Two months earlier I had given a plenary talk at the MESON conference in Kraków. I usually don't write proceedings, but this time my experimental colleagues from the GlueX collaboration needed one. They had used formulas I derived that are not yet published, because the paper is not finished. A PhD student who did the analysis wanted to present his preliminary results in a proceeding of his own, and he needed a reference for the formalism. So they asked me to write a proceeding they could cite.

The request came on Slack while I was at another conference, listening to talks. I had no time to write it myself.

## What I did

1. **Created a new folder** for the proceeding and put in it:
    - the slides of my MESON talk,
    - my analysis note, the one I will later use to write the full paper,
    - the LaTeX template downloaded from the conference website.

2. **Gave Claude access to everything** in the folder.

3. **Wrote one long prompt** telling Claude the whole story:
    - I gave a plenary talk at this conference, with the link to the conference website.
    - The slides are the content of the talk, and the analysis note contains the formalism.
    - Why the proceeding is needed: my GlueX colleagues and their PhD student must be able to cite the formalism before the paper is out.
    - The proceeding must follow the conference template.

4. **Read the draft.** About half an hour later the proceeding was written.

5. **Finished it by hand:**
    - removed one sentence that was not appropriate,
    - added my email and my grant numbers,
    - submitted it to arXiv and to the conference proceedings.

## Result

The proceeding was clear, concise, exactly what I wanted, and formatted the way the conference required. Apart from the one sentence I removed, I kept the text as Claude wrote it.

It is on arXiv and INSPIRE: [Meson photoproduction at Jefferson Lab: from two-meson final states to meson-baryon spin-density matrices](https://inspirehep.net/literature/3208903). My colleagues can now cite the formalism in their own proceeding.

## What to watch for

- **Give the full context.** The long prompt with the whole story (who needs it, why, and what it must contain) is what made the first draft usable.
- **Put the real sources in the folder.** Slides, analysis note and the official template meant Claude worked from my material rather than from general knowledge.
- **Read every sentence.** One sentence was not appropriate and had to go. You remain the author.
- **Unpublished work.** The analysis note contained results that are not yet published. Check what you are allowed to share before you give Claude access. See [Data and privacy](../../getting-started/data-and-privacy.md).
- **The details are yours to add**: author email, affiliations, grant numbers, acknowledgements.
