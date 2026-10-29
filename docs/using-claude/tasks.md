# Longer tasks and scheduling

Claude no longer only answers questions. In the same conversation, you can hand it a bigger piece of work (a report, a spreadsheet, a slide deck, a literature table) and it plans the steps, works through them, and gives you finished files. This used to be a separate mode called **Cowork**; since September 2026 it is part of every chat on Pro, rolling out gradually.

!!! note "Do you have it yet?"
    If your message box still shows separate **Chat** and **Cowork** options, your account has the older layout. Everything below still works, in the **Cowork** mode.

## Hand over a task

Describe the result you want, the material to use and what good looks like, as you would to a colleague:

- *"Using the three attached papers, make a table comparing their samples, methods and constraints on σ8, then write a one-page summary for our group meeting as a Word document."*
- *"Read the CSV of last semester's exam marks (anonymised), compute the distribution per question and make five slides on which questions worked and which did not."*
- *"Go through the PDFs in my 'Referee guidelines' folder and draft a checklist I can reuse."*

Claude may ask a few questions first, then work for several minutes. You can:

- **Watch, stop or redirect** it at any time.
- **Run several tasks in parallel** in different conversations.
- **Close the laptop**: tasks started on the web or mobile keep running in the cloud, and the result appears in the conversation. You can check progress and answer questions from the mobile app.

The results come back as real files: Word documents, spreadsheets with working formulas, PowerPoint-compatible decks, PDFs, or [Artifacts](artifacts.md) (Docs, Slides, Design).

## How independently Claude works

The **permission control** in the message box decides whether Claude asks before each step:

| Setting | What happens |
|---|---|
| **Auto** (default on Pro) | Claude proceeds without asking at each step; automatic safety checks run before actions. |
| **Manual** | Claude asks before each action. |

!!! tip "Recommended while you learn"
    Switch to **Manual** for anything that touches your email, calendar, files or websites where you are logged in. Read what Claude proposes before you approve.

## Files on your computer (desktop app)

In the **desktop app**, you can give Claude access to a folder so it can read, organise and create files there. Set this up under **Settings** (look for **Storage folder** and **Trusted folders**). By default Claude asks before permanently deleting anything.

- Only grant folders you would be happy to share. Not your whole home directory, not folders with student data or collaboration-internal material. See [Data and privacy](../getting-started/data-and-privacy.md).
- Local folders, the built-in browser and computer use only work while the desktop app is open.
- **Computer use** (beta on Pro): Claude can click, type and move between apps on your screen. Powerful but slow and risky; keep it for tasks where nothing else works.

## Scheduled tasks

Ask Claude to repeat a task on a schedule: *"Every Monday at 8:00, summarise the new arXiv astro-ph.CO papers that mention weak lensing and email me the list."* Scheduled tasks run in the cloud, so they continue when your computer is off. See the [weekly arXiv digest](../examples/research/weekly-arxiv-digest.md) example.

Each run uses your allowance. Check your scheduled tasks now and then and delete the ones you no longer need.

## Skills {#skills}

A **skill** is a set of instructions (and sometimes scripts) that teaches Claude how you want a type of task done. Claude uses a skill automatically when the task comes up.

- **Built-in skills** create and edit Word, Excel, PowerPoint and PDF files. They are on by default.
- **Your own skills**: for example "how I format exercise sheets for my course" or "the ICCUB template for seminar announcements". Ask Claude in a chat to turn a workflow you just did into a skill, or upload one.
- Manage them in **Customize → Skills**. Skills need **Create and edit files** (formerly *Code execution and file creation*) switched on in **Settings → Capabilities**.
- **Plugins** bundle skills and connectors for a role. Browse them in the directory under **Customize**. Only install plugins and skills from sources you trust: they contain instructions Claude will follow.

Sharing skills with colleagues is only possible on Team plans. On Pro, share the skill file itself.

## Usage

Long tasks use much more of your allowance than a quick question. Check **Settings → Usage**, and see [Usage limits](../getting-started/what-is-claude.md#usage-limits).

## Current limits

- **Incognito chats** open in the older experience: Claude cannot create files or run code in them.
- Old Cowork tasks are in **Recents** but not in chat search.

Reference: [Claude Cowork and chat are one Claude](https://support.claude.com/en/articles/16761823-claude-cowork-and-chat-are-one-claude) (Anthropic help center).
