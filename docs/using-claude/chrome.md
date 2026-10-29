# Claude in Chrome

**Claude in Chrome** is a browser extension that lets Claude read, click and type in web pages, in a side panel next to the page. It can do multi-step tasks on websites for you: fill a form, collect information across several tabs, navigate an awkward web portal. It is included in Pro, for Google Chrome on desktop only (not other Chromium browsers, not mobile).

## Install

1. In Google Chrome (desktop), go to the Chrome Web Store and search for **Claude** by Anthropic.
2. Click **Add to Chrome**.
3. Sign in with your Claude Pro account.
4. Pin it: click the puzzle icon in the toolbar, then the pin next to Claude.
5. Click the Claude icon to open the side panel.

!!! info "What changed in autumn 2026"
    - The side panel is becoming a full Claude session (it was called a *Cowork* session): your conversations are saved, sync with your other devices, and can use your skills and connectors. This reaches Pro accounts gradually. To go back, click the three dots at the top right of the panel and choose **Switch back to classic**.
    - **Scheduled tasks**: the clock icon at the top right of the panel runs a browser task daily, weekly or monthly.
    - **Shortcuts**: save a prompt you reuse and call it by typing `/`.
    - The **desktop app** now has its own built-in browser, which Claude can use instead of Chrome during [longer tasks](tasks.md). Choose which one in **Settings → Cowork → Preferred browser**. To let the desktop app use Chrome, go to **Customize → Connectors**, click **Configure** next to Claude in Chrome and switch it on.

## What it is good for

- **Collecting information**: *"Open the registration pages of these three conferences and make a table with dates, fees, abstract deadline and early-bird deadline."*
- **Tedious portals**: *"Go through the steps on this page to download the observing log for proposal 2026A-017."* (you stay logged in yourself)
- **Reading what you are looking at**: *"Summarise this paper's abstract page and tell me if they use the same simulation suite as us."*
- **Forms**: *"Fill in this travel form with the details from the confirmation email I opened in the other tab. Don't submit."*

## Safety first

Claude in Chrome acts **as you**, in sites where you are logged in. Treat it like giving someone your laptop for a few minutes.

- **Check the permission mode.** The side panel starts in **Automatically approve**, where Claude only stops when an action needs approval. While you learn, switch to a mode that asks before each action; the panel remembers your choice.
- **Start with read-only tasks.** Let it collect and summarise before you let it type or click *Submit*.
- **Ask it to stop before submitting**: add *"Don't submit, I'll check first"* to any form task.
- **Site permissions**: Claude asks before acting on a new site. Only allow sites you need. Avoid banking, UB payroll and HR portals.
- **Untrusted pages can contain hidden instructions** aimed at AI assistants ("prompt injection"). Don't let Claude act on pages you don't trust, and watch what it does.
- Everything Claude reads on a page becomes part of your chat. See [Data and privacy](../getting-started/data-and-privacy.md).

## Chrome extension or connectors?

If a service has a [connector](connectors.md) (Gmail, Google Drive, Google Calendar, GitHub…), use the connector: it is faster and more reliable. Use Chrome for websites that have no connector, such as conference sites, journal submission systems or university portals.

Reference: [Getting started with Claude in Chrome](https://support.claude.com/en/articles/12012173-getting-started-with-claude-in-chrome) (Anthropic help center).
