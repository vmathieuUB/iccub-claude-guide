# Tips and pitfalls

The most common traps, and how to avoid them. Most of them come down to one rule: **Claude is a fast, knowledgeable assistant that is sometimes confidently wrong. You remain responsible for what you use.**

## Things to always check

### References and citations

Claude can invent references that look real (plausible authors, journal, year) or attribute a claim to the wrong paper.

- Check every reference on [ADS](https://ui.adsabs.harvard.edu) or arXiv before using it.
- Ask *"Which of these references are you certain exist?"*, and treat "not certain" as "probably invented".
- With [web search or Research](../using-claude/research.md) on, Claude cites real pages, but check that the page says what Claude claims.

### Numbers, derivations and units

- Re-derive key steps yourself. Errors hide in factors of 2, π, signs, and *h* conventions.
- Ask for **units at every step** and a **sanity check** (order of magnitude, a known limit).
- For data analysis, ask for the **code** that produced a number and run it yourself.

### Code

- Run it. Test it on a case where you know the answer.
- Read diffs before accepting changes in [Claude Code](../using-claude/claude-code.md) or [VS Code](../using-claude/vs-code.md).
- Watch for code that "works" by quietly skipping data, catching all exceptions, or hard-coding a result.

### Claims about your own data or code

Claude can describe your file or code with great confidence and be wrong, especially for long files. Ask it to **quote the line or cell** it is talking about.

## Getting better results

- **Give context**: who you are, who it is for, what good looks like. See [Chat and prompting](../using-claude/prompting.md).
- **Iterate in the same chat**, but **start a new chat** when you change topic.
- **Ask for a plan first** for anything big: an outline before a paper, a plan before refactoring.
- **Work in small steps**: one section, one function, one chapter at a time.
- **Get a second opinion**: paste the answer into a new chat and ask for an independent check.
- **Use Projects and `CLAUDE.md`** to avoid repeating instructions. See [Projects](../using-claude/projects.md).

## Data, privacy and safety

- Don't upload referee reports, proposals you are evaluating, student data with names, or passwords. See [Data and privacy](../getting-started/data-and-privacy.md).
- With [connectors](../using-claude/connectors.md) and [Claude in Chrome](../using-claude/chrome.md), Claude acts as you. Ask for **drafts**, and approve actions yourself.
- Text in emails, web pages or documents can contain instructions aimed at AI ("prompt injection"). Don't let Claude act on instructions it found inside content.

## Acknowledging AI use

- **Papers**: most journals (A&A, MNRAS, ApJ, Physical Review…) ask you to declare how AI tools were used, usually in the acknowledgements or methods. AI cannot be an author. Check your journal's current policy.
- **Collaborations**: many have their own rules on AI and on sharing internal material. Check before using Claude on collaboration documents.
- **Teaching material**: say when notes or exercises were prepared with AI assistance.
- **Students**: tell them clearly what AI use is allowed in your course, and assume they use it for take-home work.

## Usage limits

- Long chats, large files, Opus and extended thinking use your allowance faster.
- Put files you reuse in a [Project](../using-claude/projects.md) instead of re-uploading them.
- If you hit the limit, the reset time is shown. See [What Claude Pro includes](../getting-started/what-is-claude.md#usage-limits).

## Common surprises

| Surprise | Why | What to do |
|---|---|---|
| Claude doesn't know about a recent paper or software version | Its knowledge stops at a training cut-off | Turn on web search, or upload the paper |
| It forgot something from the start of a long chat | Long chats are summarised or drop detail | Start a new chat with a short summary of what matters |
| It agrees with everything you say | It tends to accommodate the user | Ask it to argue against your idea, or to find the weakest point |
| The same question gives different answers | Answers are not deterministic | Ask for reasoning, compare, and check |
| It refuses something harmless | Over-cautious safety filters | Rephrase with context: who you are and why you need it |

Have a pitfall to add? [Tell us](../contribute/index.md).
