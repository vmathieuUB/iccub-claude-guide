---
tags:
  - Teaching
  - Projects
---

# Exercise sheets with solutions, in a Project

!!! info "Illustrative example"
    This example was written by the site editors to show the workflow. It is not yet a real ICCUB experience. If you try it, [send us your version](../../contribute/index.md) and we will replace it.

| About this example | |
| --- | --- |
| **Author** | ICCUB Claude Guide editors |
| **Date** | 2026-10-06 |
| **Area** | Teaching |
| **Tools used** | claude.ai Projects, extended thinking |
| **Time saved** | About 2 hours per sheet (estimate) |

## Goal

Produce weekly problem sheets for a course, at the right level, with full solutions for the teaching assistants, and without repeating last year's problems.

## What I did

1. **Created a Project** "Electromagnetism, problem sheets" and uploaded: the syllabus, the lecture notes, last year's sheets and exams (so it can avoid repeating them).

2. **Project instructions:**

    ```text
    Course: Electromagnetism, 2nd year Physics, UB. Problem sheets in Catalan.
    Each sheet: 5 problems, increasing difficulty, covering only material taught up to that week.
    Format: LaTeX, using the exam class. Solutions in a separate file.
    Don't reuse problems from the uploaded past sheets and exams.
    Solutions must be complete, with every step, and a final numerical check.
    ```

3. **Each week**, with extended thinking on:

    > *Week 6 covered Gauss's law in matter and boundary conditions (lecture notes ch. 6). Make the sheet and the solutions.*

4. **Checked the solutions** by asking for an independent check in a **new chat** (so it doesn't just agree with itself):

    > *Here is a problem and a proposed solution. Solve it independently, then compare and point out any error.*

5. Corrected by hand and compiled.

## Result

A sheet and a solutions file each week, in about 30 minutes of review instead of 2 to 3 hours of writing.

## What to watch for

- **Solutions contain errors** surprisingly often on harder problems: units, signs, a wrong limit. The independent re-check catches some; you must catch the rest.
- **Problems can be unsolvable** as stated (missing data, inconsistent numbers). Solve them yourself or have a TA do it before publishing.
- **Originality**: problems may resemble well-known textbook ones. That is usually fine for practice, less so for exams.
