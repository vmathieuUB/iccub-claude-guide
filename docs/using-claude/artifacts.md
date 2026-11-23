# Artifacts

When Claude produces something substantial (a document, a slide deck, a design, a small interactive page), it opens it in a panel next to the chat. That is an Artifact. All your Artifacts are kept in the **Artifacts** tab of the left sidebar.

## Kinds of Artifact

Since September 2026, Artifacts come in a few types, and Sheets and Whiteboards (both in beta) are the newest. You don't need to pick one: ask for what you want and Claude chooses. You can also start from a template in the **Artifacts** tab.

| Type | Good for | Export to |
|---|---|---|
| **Docs** | A course handout, a one-page project summary, a report, meeting notes | Word, PDF, Markdown, Google Docs |
| **Slides** | A talk, a seminar, lecture slides from your notes | PowerPoint, PDF, Google Slides |
| **Design** | A poster, a one-pager, a landing page for an event, a mock-up | PDF, PowerPoint, HTML, .zip |
| **Sheets** (beta) | A spreadsheet you and Claude edit together: a grading sheet, an observing log, a budget with working formulas | .xlsx, CSV |
| **Whiteboards** (beta) | Thinking through an idea: Claude arranges notes into diagrams, flows and groups (a paper outline, a project plan) | PNG |
| **Data** (formerly *Dashboards*) | Dashboards and short data stories from a connected data source (a database or an app such as Salesforce). Mostly meant for company data; for your own data files, upload them to a chat instead. | |
| **Interactive pages** | A slider that shows how a Planck spectrum changes with temperature, a quiz for students, a simple calculator | |

Artifacts made before September 2026 still work and can still be published, but new ones use the types above.

## Working with them

- **Change it by asking**: *"Add a second slider for redshift"*, *"Make slide 4 less crowded."*
- **Edit it yourself**: type directly in a doc, edit any slide, or move elements on a design.
- **Edit one part with Claude**: select text in a doc and click **Edit with Claude**, then say what to change. Claude only touches that part.
- **Present** slides directly from Claude with **Present**, or download them.
- **Go back**: editing an earlier message in the chat starts a new branch with its own Artifacts, so the original stays intact.

If Artifacts don't appear, check that **Create and edit files** (formerly *Code execution and file creation*) is on in **Settings → Capabilities**.

## Sharing

- New Artifacts are **private** to you until you share them.
- **Share** gives you a link. Check who can open it before you send it, and don't share anything you would not put on a public web page.
- Older Artifacts (before September 2026) must be **published** to share them; anyone with the link can see and use them without an account.
- Some interactive Artifacts store data. If an Artifact uses **shared storage**, everyone who opens it sees what is entered. Don't type sensitive data into one.

## Examples

!!! example "Slides for a seminar"
    *"From the attached paper, make 12 slides for a 30-minute ICCUB seminar: motivation, method, three key results with the figures from the paper, and an outlook slide. Use a plain white style with large fonts."*

!!! example "An interactive plot for a class"
    *"Make an interactive page with a slider for the temperature of a black body from 3 K to 30 000 K. Show the Planck spectrum on a log-log plot, mark the Wien peak, and print the peak wavelength. Add a toggle for wavelength vs frequency."*

!!! example "A quiz"
    *"Make a 10-question multiple-choice quiz on stellar evolution for first-year students. Show the right answer and a one-line explanation after each answer. Show a score at the end."*

!!! example "A one-page summary"
    *"Turn the attached proposal into a one-page summary doc for the ICCUB website, with a title, three short paragraphs and a 'Key numbers' box. Export it as Word."*

## Limits

- Interactive Artifacts run in the browser. They are not a replacement for real analysis code.
- Check physics and numbers in an Artifact just as you would in a chat answer: a nice-looking slide or slider can still use the wrong formula.
- Exported PowerPoint or Word files may need layout fixes; open them before you present or send them.

References: [What are artifacts and how do I use them?](https://support.claude.com/en/articles/17153992-what-are-artifacts-and-how-do-i-use-them), [Claude Sheets](https://support.claude.com/en/articles/18324300-get-started-with-claude-sheets), [Claude Whiteboards](https://support.claude.com/en/articles/18324319-get-started-with-claude-whiteboards), [Claude Data](https://support.claude.com/en/articles/17454700-get-started-with-claude-data) (Anthropic help center).
