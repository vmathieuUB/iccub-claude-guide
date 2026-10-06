---
tags:
  - Research
  - Claude Code
  - VS Code
  - Coding
---

# Clean up and test an analysis pipeline in VS Code

!!! info "Illustrative example"
    This example was written by the site editors to show the workflow. It is not yet a real ICCUB experience. If you try it, [send us your version](../../contribute/index.md) and we will replace it.

| About this example | |
| --- | --- |
| **Author** | ICCUB Claude Guide editors |
| **Date** | 2026-10-06 |
| **Area** | Any computational work |
| **Tools used** | Claude Code extension in VS Code, Python, pytest, git |
| **Time saved** | About two days (estimate) |

## Goal

A PhD student is leaving and handing over a 3000-line Python analysis (one big script plus notebooks) to a new student. We want it understandable, tested and reproducible before the handover, without changing the scientific results.

## What I did

1. **Opened the repository folder in VS Code** and made sure everything was committed in git.

2. **Asked for a tour, no changes:**

    > *Explain what this project does, the data flow from raw files to final plots, and which functions are the most fragile. Don't change anything.*

3. **Froze the current results first.** Before any refactoring:

    > *Write a script `tests/make_reference.py` that runs the full pipeline on `data/sample/` and saves every output array to `tests/reference/`. Then write a pytest test that reruns the pipeline and checks the outputs match the reference to 1e-10.*

    Ran it once, checked the reference outputs by eye, committed.

4. **Refactored in small steps with `/plan`:**

    > */plan Split analysis.py into modules (io, cleaning, fitting, plotting) without changing behaviour. Propose the split first.*

    After agreeing on the plan: *"Do step 1 only, then run the tests."* Repeated step by step, reading every diff.

5. **Added unit tests** for the core functions: *"Write tests for `fit_profile` including edge cases: empty input, NaNs, a single point."* Two tests failed, revealing a real bug with NaN handling, which we fixed separately and documented.

6. **Wrote documentation**: a `README.md` with install and run instructions, docstrings, and a `CLAUDE.md` for whoever uses Claude on it next.

## Result

Same numerical results (regression test passing), five modules instead of one script, 25 unit tests, a README, and one genuine bug found and fixed.

## What to watch for

- **Freeze results before refactoring.** Without the regression test, small behaviour changes (sorting, float precision, default arguments) slip through.
- **Small steps.** "Refactor everything" produces a diff too big to review.
- **Tests written by Claude can be wrong too**: a test that checks the buggy behaviour just locks the bug in. Read them.
- **Don't let it "fix" the physics** while refactoring. Ask it to list suspicious physics separately instead of changing it.
