# Uploading files

Drag files into the chat, or click **+** next to the message box. Claude then reads them as part of the conversation.

## What you can upload

| Type | Formats | What Claude sees |
|---|---|---|
| Documents | PDF, DOCX, TXT, RTF, ODT, HTML, EPUB | Text. For PDFs under 100 pages, also figures, plots and tables. |
| Data | CSV, JSON, XLSX | The content. With code execution on, Claude can also analyse it with Python. |
| Code | `.py`, `.ipynb`, `.c`, `.f90`, `.tex` and other text files | The text |
| Images | PNG, JPEG, GIF, WebP | The image: plots, photos of a whiteboard, screenshots, handwritten notes |

Limits: up to **30 MB per file** and **20 files per chat**. Only text is read from PDFs longer than about 1000 pages. Images work best at 1000 px or more on a side.

!!! warning "Before you upload"
    Check [Data and privacy](../getting-started/data-and-privacy.md). No referee reports, no student data with names, no collaboration-internal material unless you have checked the rules.

## Papers

- *"Summarise the method and list the main assumptions."*
- *"What do they use for the halo mass function, and how does it differ from Tinker et al.?"* (upload both papers)
- *"Explain Figure 4 to a master's student."*
- *"Write a 150-word summary for our group journal club announcement."*

Claude reads the figures in a PDF, so you can ask about plots directly. Check anything you plan to quote: Claude can misread a number from a plot.

## Data

With **Code execution and file creation** turned on (Settings → Capabilities), Claude can run Python on an uploaded CSV or Excel file: compute statistics, fit a model, make a plot, and give you the resulting file.

- *"Plot column `flux` against `mjd`, with error bars from `flux_err`, and mark points with `flag == 1` in red."*
- *"Fit a power law to this spectrum between 1 and 10 keV and give me the index with an uncertainty."*

Ask for the code too, so you can rerun and check it on your own machine.

## Images and screenshots

- A photo of a whiteboard: *"Turn this into LaTeX."*
- A plot from a colleague: *"What is wrong with this figure for a paper?"*
- A screenshot of an error message: *"What does this mean and how do I fix it?"*

## Files you use again and again

If you keep uploading the same syllabus, paper or style guide, put it in a [Project](projects.md) instead. Every chat in the Project sees it, and it uses less of your allowance than re-uploading.
