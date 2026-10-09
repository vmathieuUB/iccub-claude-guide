# Your first 30 minutes

You just got a Claude account: your own Pro plan or a seat on your group's Team plan (see [How to get Claude](get-claude.md)). Here is what to do before your first real task. Each step takes a few minutes.

## 1. Sign in and check your plan

Go to [claude.ai](https://claude.ai) and sign in with the email your account was created with. Open **Settings → Billing** (click your name, bottom left) and check that it says **Pro** (on a Team seat, your group's name appears instead). If it says Free, you are signed in with the wrong email.

## 2. Check your privacy settings

Open **Settings → Privacy**. The setting **Help improve Claude** decides whether your chats can be used to train future models.

!!! warning "Recommended for ICCUB"
    Turn **Help improve Claude** off if you will discuss unpublished results, collaboration data, referee reports or student work. Read [Data and privacy](data-and-privacy.md) before uploading anything sensitive.

## 3. Tell Claude who you are

Open **Settings → Profile** and fill in:

- **What best describes your work**: for example *Research* or *Education*.
- **Personal preferences**: short instructions Claude follows in every chat. For example:

```text
I am an astrophysicist at the Institute of Cosmos Sciences (ICCUB),
University of Barcelona. I work mostly in Python and LaTeX.
Answer concisely, use SI or cgs units as appropriate, and say
clearly when you are unsure or when a reference should be checked.
```

You can change this at any time.

## 4. Install the apps (optional)

The web version is enough to start. If you want more:

- **Desktop app** for macOS and Windows, from [claude.ai/download](https://claude.ai/download).
- **Mobile app** for iOS and Android, from your app store. Your chats sync across all of them.
- **Claude Code**, for working on code in your terminal or VS Code, is covered in [Claude Code](../using-claude/claude-code.md).

More detail in [What Claude Pro includes](what-is-claude.md).

## 5. Have a first conversation

Start a new chat and try something you actually need this week. A few ideas:

- *"Explain the difference between a Markov chain Monte Carlo and nested sampling, for a first-year PhD student."*
- Upload a paper PDF and ask: *"Summarise the method and list the main assumptions."*
- Paste a Python function and ask: *"Find bugs and suggest clearer variable names."*
- *"Draft a short email to my students announcing that next week's class moves to room 503."*

If the first answer is not right, reply and say what to change. Iterating in the same chat usually works better than starting over. See [Chat and prompting](../using-claude/prompting.md).

## 6. Know the main controls

| Control | Where | What it does |
|---|---|---|
| Model picker | Below the message box | Pick a model. The default is fine for most work; the larger model is slower but better at hard reasoning. |
| Extended thinking | Same menu | Claude thinks longer before answering. Useful for derivations and tricky code. |
| **+** button | Left of the message box | Upload files, turn on web search, connect tools. |
| Projects | Left sidebar | Keep files and instructions together for one course or paper. See [Projects](../using-claude/projects.md). |

## 7. Know the usage limits

Pro has generous but finite usage. Long chats, large files and the larger model use your allowance faster. If you hit the limit, Claude tells you when it resets (usually within a few hours). Starting a new chat for a new topic, instead of continuing a very long one, makes your allowance last longer.

## 8. Keep your judgement on

Claude can be confidently wrong. Always check citations, numbers and derivations before you reuse them. [Tips and pitfalls](../tips/index.md) lists the common traps.

## Next steps

- [What Claude Pro includes](what-is-claude.md): the full list of features.
- [How to use Claude](../using-claude/index.md): one page per feature.
- [Examples](../examples/index.md): what other ICCUB members do with it.
