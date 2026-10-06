# Artifacts

When Claude produces something substantial and self-contained (a document, a piece of code, a diagram, a small interactive page), it opens it in a panel next to the chat. That is an Artifact.

## What they are good for

- **Documents**: a course handout, a one-page project summary, a FAQ.
- **Diagrams**: a flowchart of your data pipeline, a timeline of the Universe (SVG or Mermaid).
- **Interactive pages**: a slider that shows how a Planck spectrum changes with temperature, a quiz for students, a simple calculator.
- **Code**: a script you will copy into your project.

Claude decides when to create one, but you can ask: *"Make this an artifact."*

## Working with them

- **Change it by asking**: *"Add a second slider for redshift"*, *"Make the font bigger."* Claude updates the Artifact and keeps earlier versions; use the arrows in the panel to go back.
- **Copy or download**: buttons in the top corner of the panel.
- **Publish**: the **Publish** or **Share** button gives you a public link. Anyone with the link can see (and use) it without an account. Don't publish anything you would not put on a public web page.

If Artifacts don't appear, check that **Code execution and file creation** is on in Settings → Capabilities.

## Examples

!!! example "An interactive plot for a class"
    *"Make an interactive page with a slider for the temperature of a black body from 3 K to 30 000 K. Show the Planck spectrum on a log-log plot, mark the Wien peak, and print the peak wavelength. Add a toggle for wavelength vs frequency."*

!!! example "A quiz"
    *"Make a 10-question multiple-choice quiz on stellar evolution for first-year students. Show the right answer and a one-line explanation after each answer. Show a score at the end."*

!!! example "A one-page summary"
    *"Turn the attached proposal into a one-page summary for the ICCUB website, with a title, three short paragraphs and a 'Key numbers' box."*

## Limits

- Interactive Artifacts run in the browser. They are not a replacement for real analysis code.
- Check physics and numbers in an Artifact just as you would in a chat answer: a nice-looking slider can still use the wrong formula.
