---
tags:
  - Outreach
  - Artifacts
---

# An animated web page for a public event

!!! info "Illustrative example"
    This example was written by the site editors to show the workflow. It is not yet a real ICCUB experience. If you try it, [send us your version](../../contribute/index.md) and we will replace it.

| About this example | |
| --- | --- |
| **Author** | ICCUB Claude Guide editors |
| **Date** | 2026-10-06 |
| **Area** | Outreach |
| **Tools used** | claude.ai Artifacts, then Claude Code for the final version |
| **Time saved** | Days of web development, for someone who doesn't build websites (estimate) |

## Goal

For an open day stand, make an interactive page that visitors can play with on a tablet: **"Build a solar system"**, where you place planets around a star and watch the orbits, with a short explanation of Kepler's laws. No web development skills needed.

## What I did

1. **Described it in a chat**, asking for an Artifact:

    > *Make an interactive web page for a science fair, for visitors aged 10 and up. A star in the centre; visitors tap to add planets at different distances; planets orbit with realistic Kepler speeds (inner ones faster). Show each planet's orbital period. A "Explain" button opens a three-sentence explanation of Kepler's third law. Big buttons, works on a tablet, colourful but not childish. Text in Catalan, Spanish and English with a language switch.*

2. **Iterated by playing with it**, in the same chat:

    > *Planets are too small on a tablet. Add trails behind the planets. Add a "reset" button. When two planets are too close, show a warning "Unstable orbit!".*

3. **Checked the physics**: *"Show me the formula you use for the period and the units."* Verified that doubling the distance gives a period × 2.83.

4. **Published it** with the Artifact's **Publish** button to get a link and a QR code for the stand. For a permanent version on the ICCUB website, downloaded the HTML file and gave it to the web team.

## Result

A working, bilingual, touch-friendly page in about an hour, used on a tablet at the stand. Children played with it; parents read the explanation.

## What to watch for

- **Physics shortcuts**: animations often fake the physics (circular orbits, wrong speed ratios). Ask what is computed and check.
- **Translations**: have a native speaker check the Catalan and Spanish texts.
- **Published Artifacts are public**: anyone with the link can see them. Nothing confidential in them.
- **Test on the real device** before the event: tablets differ in screen size and touch behaviour.
- For something bigger (several pages, maintained over years), use [Claude Code](../../using-claude/claude-code.md) on a proper repository instead of an Artifact.
