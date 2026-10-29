# Claude Science

**Claude Science** is Anthropic's desktop app for scientific research, in **beta** since June 2026 and included in Pro. You describe an analysis in plain language; Claude writes and runs the code in a sandbox, reads the folders you give it, can connect to scientific databases and to your own compute, and saves every result with a record of how it was produced.

!!! note "Mostly built for the life sciences, for now"
    Its curated skills and database connectors are aimed at biology and chemistry (genomics, proteins, PubMed…). There is nothing physics- or astronomy-specific yet, such as ADS or astropy-aware tools. For most ICCUB work, [Claude Code](claude-code.md) in a terminal or [VS Code](vs-code.md) is the more mature choice. Claude Science is worth a try if you want its provenance records or its job submission to a cluster.

## Install

1. Download it from the [Claude Science page](https://claude.com/product/claude-science). It runs on macOS 13 or later, Windows 11 (x64) and Linux x64.
2. Sign in with your Claude Pro account.

If you are on a group's **Team plan for scientists**, it is switched on by default. On other Team plans, the plan owner enables it.

## What it does

- **Runs analyses end to end**: writes and runs Python in a sandbox, on files in a folder you provide.
- **Keeps the provenance**: each figure or table is saved with its code, environment and conversation, so you (or a referee) can reproduce it later, and ask for edits in plain language.
- **Uses your compute**: it drafts a plan, asks before using new resources, and can submit jobs to an HPC cluster over SSH.
- **Checks its own work**: a reviewer agent looks at citations and calculations and flags errors. Still check them yourself.
- **Forks a session** so you can compare two approaches.

## Ideas for ICCUB

- *"Load the light curves in `data/`, fit a damped random walk to each, and make a table of the best-fit timescales with uncertainties."*
- *"Reproduce Figure 3 of the attached paper from the public catalogue, and tell me where our result differs."*
- *"Prepare and submit a job array on our cluster that runs `run_mcmc.py` for each of the 20 parameter files, then collect the chains when they finish."*

## Stay in control

- Point it at a **copy** of your data, or a folder you are allowed to share. Data stays on your machine or cluster, but the parts needed for each step are sent to Claude. See [Data and privacy](../getting-started/data-and-privacy.md).
- Read the plan before it uses cluster time.
- It is a beta: expect rough edges and check results as you would a student's first analysis.

Reference: [Get started with Claude Science](https://support.claude.com/en/articles/16563838-get-started-with-claude-science) (Anthropic help center).
