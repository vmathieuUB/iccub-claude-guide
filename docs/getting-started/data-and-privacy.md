# Data and privacy

What happens to what you type and upload, and what you should keep out of Claude.

!!! info "Not legal advice"
    This page summarises Anthropic's public policies as of October 2026. For anything that matters, check the [Anthropic Privacy Center](https://privacy.claude.com) and the UB data protection rules.

## What happens to your data

Claude Pro is a **consumer** plan. Your chats are covered by Anthropic's [Consumer Terms](https://www.anthropic.com/legal/consumer-terms) and [Privacy Policy](https://www.anthropic.com/legal/privacy), not by a contract with UB.

**Model training is your choice.** The **model improvement** setting (Settings → Privacy, labelled **Help Improve our AI models**) decides whether your chats and Claude Code sessions can be used to train future models.

| Setting | Used for training? | How long Anthropic keeps your chats |
|---|---|---|
| **Off** (recommended) | No | Deleted chats are removed within 30 days |
| **On** | Yes | Up to 5 years, in de-identified form |

A few details:

- **Deleted chats** are not used for future training, whatever the setting.
- **Incognito chats** (an option when starting a new chat) are never used for training and do not appear in your history.
- **Thumbs up / down feedback** sends that whole conversation to Anthropic, who may keep it for up to 5 years and use it for training, even with the setting off. Don't rate chats that contain sensitive material.
- **Chats flagged for safety review** may be kept longer (up to 2 years).
- **Connectors** (Google Drive, Gmail and so on) let Claude read what you point it to in that chat. That content is then part of the chat.
- **Folders on your computer** that you open to Claude in the desktop app, [Claude Code](../using-claude/claude-code.md) or [Claude Science](../using-claude/science.md): what Claude reads from them is sent to Anthropic like an upload.

## Memory {#memory}

Claude keeps a **memory** of useful context from your chats (your field, your courses, how you like answers), stored as separate topics. It is on by default on Pro.

- **See and edit it**: **Settings → Your Claude**, then **Manage** next to *Your memory*. Open a topic to read, edit or delete it. You can also tell Claude in a chat to remember or forget something.
- **Turn it off**: the **Memory from chats** toggle in the same place. Pausing keeps what is stored; resetting deletes it all.
- **One chat without memory**: click **+** and switch off Memory before the first message, or use an incognito chat.
- **Projects** have their own memory. To keep a Project completely separate from the rest, turn off **Use account memory** on the Project page.
- **Sensitive topics** (health, politics, religion…) are not saved unless you turn on **Include sensitive topics in memory**. Leave it off.
- **Chat search**: Claude can also search your past chats when it helps. Switch this off with **Search and reference chats** in **Settings → Your Claude**.

Memory is handy, but it also means something from one chat can show up in another. Turn it off for a chat about a confidential topic.

## What you can share

A simple rule: **only upload what you would be comfortable emailing to a colleague outside UB.** Then use the table below.

| Material | OK? | Notes |
|---|---|---|
| Published papers, public data, textbooks | Yes | |
| Your own code and analysis scripts | Yes | Remove passwords, tokens and API keys first. |
| Your own drafts and unpublished results | Usually | With training off. Check you are not bound by an embargo. |
| Collaboration data and internal documents (Gaia, LSST, Euclid, LHCb, CTA…) | **Check first** | Many collaborations have their own AI or data-sharing rules. When in doubt, ask the collaboration. |
| Referee reports and papers you are reviewing | **No** | Most journals forbid uploading manuscripts under review. |
| Grant proposals you are evaluating | **No** | Evaluation is confidential; check the funder's rules. |
| Student work, grades, emails with names | **No**, unless anonymised | Personal data falls under GDPR. Remove names and IDs. |
| Personal data of anyone (CVs, health, HR) | **No** | |
| Passwords, SSH keys, API tokens | **Never** | |

## Good habits

1. **Turn model improvement off** in Settings → Privacy, unless you have a reason not to.
2. **Anonymise** before you paste: replace names with *Student A*, remove email addresses and IDs.
3. **Use an incognito chat** for one-off questions about something sensitive. It is not saved to your history or memory.
4. **Delete chats** you no longer need.
5. **Credit AI use.** Many journals ask you to state how AI was used. See [Tips and pitfalls](../tips/index.md).

## When to use a local model instead

If the data cannot leave ICCUB at all, run an open model on your own machine or an ICCUB server. Nothing is sent to an outside company. The models are weaker than Claude, but often good enough for summarising, reformatting or code help.

- [Run a local LLM on your laptop](../examples/research/local-llm-laptop.md)
- [Share a local LLM over the network](../examples/research/local-llm-remote-access.md)

## Sources

- [Is my data used for model training?](https://privacy.claude.com/en/articles/10023580-is-my-data-used-for-model-training) (Anthropic Privacy Center)
- [How long do you store my data?](https://privacy.claude.com/en/articles/10023548-how-long-do-you-store-my-data) (Anthropic Privacy Center)
- [Chat search and memory](https://support.claude.com/en/articles/11817273-use-claude-s-chat-search-and-memory-to-build-on-previous-context) (Anthropic help center)
- [Updates to Consumer Terms and Privacy Policy](https://www.anthropic.com/news/updates-to-our-consumer-terms) (Anthropic, 2025)
