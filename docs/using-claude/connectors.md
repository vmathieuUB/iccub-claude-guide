# Connectors

Connectors let Claude read from (and sometimes act in) other services you use: Google Drive, Gmail, Google Calendar, Microsoft 365, GitHub, Notion and others.

## When they help

- *"Find the latest version of the ERC proposal in my Drive and list what is still missing."*
- *"What meetings do I have next week, and which clash with my teaching?"*
- *"Summarise the open issues in our pipeline's GitHub repository."*
- *"Find the email from the journal about my revision deadline."*

Without connectors you would download and upload each file yourself.

## Connect a service

1. Open **Settings → Connectors** (also reachable from **+** in a chat).
2. Find the service and click **Connect**.
3. Sign in to that service and approve the access it asks for.

Use your **UB account** for UB Google or Microsoft services, so Claude sees work files and not personal ones (or the reverse, if that is what you want).

In a chat, open **+** to switch individual connectors on or off. Leave on only the ones that chat needs.

## What Claude can see

- Claude can access what **your account** can access in that service, but only reads what is relevant to your request.
- What it reads becomes part of that chat, under the same rules as a file you upload. See [Data and privacy](../getting-started/data-and-privacy.md).
- Some connectors can also **act**: create a calendar event, draft an email. Claude asks for your confirmation before doing so. Read the confirmation before you approve.

!!! warning
    Connecting your UB email or Drive gives Claude access to whatever is in there, including other people's data. Point it at specific files or folders, and disconnect services you no longer use (Settings → Connectors → **Disconnect**).

## More

- [Email, calendar and documents](email-calendar.md): Gmail, Google Calendar, Drive and Microsoft 365 in detail.
- [Claude in Chrome](chrome.md): for websites that have no connector.

## Tips

- Be specific about where to look: *"in the folder 'Teaching 2026'"* is faster and safer than *"in my Drive"*.
- Combine with [Research](research.md): Claude can search the web and your Drive in the same investigation.
- For GitHub, the connector lets Claude read repositories. To have Claude change code, use [Claude Code](claude-code.md).
