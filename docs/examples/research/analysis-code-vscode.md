---
tags:
  - Research
  - Claude Code
  - Coding
---

# Speed up the code behind a published paper

| About this example | |
| --- | --- |
| **Author** | Vincent Mathieu |
| **Date** | 2026-10-09 |
| **Area** | Hadron physics (theory) |
| **Tools used** | Claude Code, Google Antigravity (Gemini) and a local model, each given access to the code folder |
| **Time saved** | Review done in about half an hour; the code now runs more than 10 times faster |
| **Paper** | [High-energy η(′)π photoproduction and the nature of exotic waves](https://inspirehep.net/literature/3070423), G. Montaña, V. Mathieu et al., Phys. Lett. B 872 (2026) 140101 ([arXiv:2510.14549](https://arxiv.org/abs/2510.14549)) |

## Goal

In 2025 we published a paper with Gloria Montaña and colleagues on high-energy ηπ production. The model has five variables, and computing the observables meant integrating over four of them.

I wrote the Monte Carlo code myself, fairly quickly, partly while travelling. I deliberately used **no libraries**: I wanted to understand every step, so every routine was written by hand, from the Monte Carlo integration to the determinant of a 6×6 matrix used to check the boundaries of the physical region. It worked, and it was used for the paper, but a full run took hours.

A year later, when I started using AI coding tools, I wanted to know whether this code could be made faster.

## What I did

1. **Gave the tool access to the folder** with the code that produced the published results.
2. **Explained the context**: the paper, and that this was the code used for it.
3. **Asked for a review**, in substance: *"This is the code that was used to publish this paper. Look at all the files and check whether we can optimise it."*
4. **Repeated the exercise with three tools**: Google Antigravity (with Gemini), Claude (Sonnet, in Claude Code) and a local model, to see whether they would reach the same conclusions.

## Result

The review took about half an hour. It found:

- **Duplicated work**: several places where the same quantity was computed twice, each worth a factor of 2.
- **Inefficient routines**: my hand-written determinant routine was not efficient.

Together these gave **a speed-up of more than a factor of 10**. A year after the paper, the same code runs much, much faster.

All three tools (Antigravity, Claude and the local model) led to the same conclusion: the code became much more efficient after the AI review.

## What to watch for

- **Write it yourself first.** I think it is a good idea to start by coding every function yourself, without libraries, so that you understand both the physics and the code.
- **Then optimise with AI.** Once the code works and has been checked, and you need it efficient to produce the real numbers, ask an AI to optimise it. You keep the understanding *and* get efficient code.
- **Check the results are unchanged.** Compare the optimised code's output with the published numbers before using it.
- **Any tool will do.** Here a cloud tool and a local model found the same improvements; if your code cannot leave your machine, see [Run a local LLM on your laptop](local-llm-laptop.md).
