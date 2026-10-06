# Data and privacy

What happens to what you type and upload, and what you should keep out of Claude.

!!! info "Not legal advice"
    This page summarises Anthropic's public policies as of October 2026. For anything that matters, check the [Anthropic Privacy Center](https://privacy.claude.com) and the UB data protection rules.

## What happens to your data

Claude Pro is a **consumer** plan. Your chats are covered by Anthropic's [Consumer Terms](https://www.anthropic.com/legal/consumer-terms) and [Privacy Policy](https://www.anthropic.com/legal/privacy), not by a contract with UB.

**Model training is your choice.** The setting **Help improve Claude** (Settings → Privacy) decides whether your chats and Claude Code sessions can be used to train future models.

| Setting | Used for training? | How long Anthropic keeps your chats |
|---|---|---|
| **Off** (recommended) | No | Up to 30 days after you delete them |
| **On** | Yes | Up to 5 years |

A few details:

- **Deleted chats** are not used for future training, whatever the setting.
- **Incognito chats** (an option when starting a new chat) are never used for training and do not appear in your history.
- **Thumbs up / down feedback** sends that whole conversation to Anthropic, who may keep it for up to 5 years and use it for training, even with the setting off. Don't rate chats that contain sensitive material.
- **Chats flagged for safety review** may be kept longer.
- **Connectors** (Google Drive, Gmail and so on) let Claude read what you point it to in that chat. That content is then part of the chat.

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

1. **Turn training off** in Settings → Privacy, unless you have a reason not to.
2. **Anonymise** before you paste: replace names with *Student A*, remove email addresses and IDs.
3. **Use an incognito chat** for one-off questions about something sensitive.
4. **Delete chats** you no longer need.
5. **Credit AI use.** Many journals ask you to state how AI was used. See [Tips and pitfalls](../tips/index.md).

## When to use a local model instead

If the data cannot leave ICCUB at all, run an open model on your own machine or an ICCUB server. Nothing is sent to an outside company. The models are weaker than Claude, but often good enough for summarising, reformatting or code help.

- [Run a local LLM on your laptop](../examples/research/local-llm-laptop.md)
- [Share a local LLM over the network](../examples/research/local-llm-remote-access.md)

## Sources

- [Is my data used for model training?](https://privacy.claude.com/en/articles/10023580-is-my-data-used-for-model-training) (Anthropic Privacy Center)
- [Updates to Consumer Terms and Privacy Policy](https://www.anthropic.com/news/updates-to-our-consumer-terms) (Anthropic, 2025)
