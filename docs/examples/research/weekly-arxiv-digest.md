---
tags:
  - Research
  - Scheduled tasks
---

# A weekly arXiv digest, delivered every Monday

| About this example | |
| --- | --- |
| **Author** | Vincent Mathieu |
| **Date** | 2026-10-12 |
| **Area** | Hadron physics (theory) |
| **Tools used** | A Claude scheduled task, the public INSPIRE-HEP API |
| **Time saved** | The Monday scan of new papers, every week |

## Goal

Every week dozens of papers appear in hep-ph, nucl-th and hep-lat. I wanted one short list on Monday morning with two things: the new papers that cite my work, and the new papers on my own topics (Regge theory, photoproduction, amplitude analysis, exotic hadrons, glueballs, sum rules, lattice spectroscopy), each with one or two sentences on why it matters to me.

Instead of asking Claude for this every week, I wrote the request once and made it a **scheduled task**: Claude runs the same prompt by itself at a fixed time and leaves the result for me to read.

## What I did

1. **Chose the source.** [INSPIRE-HEP](https://inspirehep.net) has a free public API that needs no login. It knows who cites whom, which arXiv listings alone do not. I identify myself with my INSPIRE author ID (`V.Mathieu.1`, shown on your INSPIRE author page).

2. **Wrote the queries as complete URLs.** One for citations of my work, three for my topics. Each URL is written out in full in the prompt (see the warning below on why).

3. **Wrote the prompt.** It says who I am, what to fetch, what to keep, and what the digest must look like. A shortened version you can adapt:

    ```text
    This is an automated run of a scheduled task. The user is not present to
    answer questions. Do not ask clarifying questions, do not take any "write"
    actions; if in doubt, report what you found.

    You are producing a weekly literature digest for <your name>, working on
    <your topics>, INSPIRE author ID "<your ID>", mostly in arXiv categories
    <your categories>.

    Use the INSPIRE-HEP public API. Fetch each URL below exactly as written.

    Step 1, papers citing my work. Fetch:
    https://inspirehep.net/api/literature?sort=mostrecent&size=25&q=refersto:a%20<your ID>&fields=titles,abstracts,arxiv_eprints,authors,earliest_date
    Keep only entries whose earliest_date is in the last 7 days.
    If this query fails, say so instead of reporting "no citations".

    Step 2, new papers on my topics. Fetch:
    https://inspirehep.net/api/literature?sort=mostrecent&size=20&q=(t%20<topic 1>%20or%20t%20<topic 2>)&fields=titles,abstracts,arxiv_eprints,authors,earliest_date
    (one URL per group of topics)
    Keep the last 7 days, aim for 10 to 15 papers, favour close matches.

    Step 3, remove duplicates between steps 1 and 2.

    Step 4, present two sections: "Papers citing your work" and "New papers
    on your topics". For each paper: title, first author (et al. if more
    than 3), arXiv link, and 1 to 2 sentences on why it is relevant to me.
    Keep it short and scannable.
    ```

4. **Ran it once by hand** and checked the result against INSPIRE before scheduling anything.

5. **Scheduled it**: every Monday at 08:00, Madrid time. You can ask Claude directly, *"Make this a scheduled task that runs every Monday at 8:00"*, and it shows up in your list of scheduled tasks, where you can pause, edit or run it on demand.

## Result

On Monday I open the run and find the digest. This week it listed eleven papers citing my work, among them a reanalysis of the X(2370) in J/ψ radiative decays and a lattice study of fully charmed tetraquarks, each with an arXiv link and a two-line summary. It also said plainly that none of the topic queries had anything newer than September, so I knew the section was empty, not broken.

## What to watch for

- **Nobody is there to click "Allow".** A scheduled task runs while you are away. The first automatic run of this one failed: every web request needed a permission I was not there to give, and Claude reported that it had no papers instead of inventing some. Run the task once by hand, accept the permissions it asks for, and check the next automatic run.
- **Write the URLs in full.** The web fetch tool only opens URLs that appear exactly in the prompt, so Claude cannot build a query from a template at run time. Very long URLs are also refused, so split long topic lists into several short queries.
- **Ask it to report failures.** "If this query fails, say so" turns a silent empty section into a clear message.
- **Check what it summarises.** Results pass through a summariser, and a few "citing" papers turned out unrelated (nuclear PDFs, accelerator software). Open INSPIRE before you cite anything.
- **One run, one report.** Ask for a chat message, not a file, and no "write" actions: an unattended task should read and report, not change things for you.
- **It uses your Pro allowance.** Each run counts like a normal conversation. Weekly is cheap; every hour is not.
