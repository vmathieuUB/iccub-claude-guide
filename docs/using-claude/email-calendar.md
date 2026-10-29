# Email, calendar and documents

With [connectors](connectors.md), Claude can search your email, read attachments in your Drive, check your calendar and draft replies. This is the most useful set-up for admin work: travel, reimbursements, meeting planning, reports.

## Which connector

| Your account | Connector | What Claude can do |
|---|---|---|
| Gmail / Google account | **Gmail**, **Google Calendar**, **Google Drive** | Search and read email, draft, reply and send (asks first); view, create and change events; find free slots; search, read and save Drive files |
| Google account | **Google Docs**, **Google Sheets**, **Google Slides** | Edit a file live in a pane next to the chat, create new ones, work with Docs comments and suggestions |
| UB Microsoft 365 (Outlook, OneDrive, SharePoint, Teams) | **Microsoft 365** | Search email, calendar, OneDrive, SharePoint and Teams. Since July 2026 it can also draft and send email, manage events and edit OneDrive/SharePoint files, but only once the administrator has enabled these write tools |

!!! warning "Microsoft 365 needs UB IT"
    The Microsoft 365 connector only works with a work account, once a Microsoft administrator of the organisation has approved it once (write tools need a second approval). Personal accounts such as @outlook.com are not supported. If it says approval is required for your UB account, contact UB IT; until then, use the Gmail connector for a Google account, or forward the relevant emails and upload attachments by hand.

## Connect

1. In a chat, click **+**, then **Connectors** (or go to **Customize → Connectors**).
2. Click **Connect** next to Gmail, Google Calendar, Google Drive, Google Docs/Sheets/Slides or Microsoft 365.
3. Sign in with the account you want Claude to use and approve the access.
4. In each chat, use **+** to switch connectors on or off. Leave on only what that chat needs.

## Things to ask

**Email**

- *"Find all emails from the SOC of the conference in Lisbon and list what they ask me to do, with deadlines."*
- *"Summarise the thread about the new GPU node and tell me who is waiting for an answer from me."*
- *"Draft a polite reply declining the referee request, suggesting Dr. X instead. Don't send it."*

**Calendar**

- *"What does my week look like? Flag anything that clashes with my Tuesday and Thursday classes."*
- *"Find three 1-hour slots in the next two weeks where Anna, Marc and I are all free."* (works if their calendars are shared with you)
- *"Create an event on Friday 15:00 to 16:00, 'Group meeting', room 503, and add the agenda from my last email to Pau."*

**Combined**

- *"Every Friday at 16:00, list the emails from this week that are still waiting for an answer from me."* (a [scheduled task](tasks.md#scheduled-tasks))
- *"I'm back from the conference in Lisbon. Find the registration receipt, flight and hotel confirmations in my email, list the amounts and dates, and draft the reimbursement email to the department administration."* See the full example: [Conference trip reimbursement](../examples/admin/conference-reimbursement.md).

## Claude inside Office: the Microsoft 365 add-ins

Separately from the connector, **Claude for Microsoft 365** puts Claude in a side panel inside **Excel**, **Word** and **PowerPoint** (and **Outlook**, in beta). Install them from [claude.com/claude-for-microsoft-365](https://claude.com/claude-for-microsoft-365) and sign in with your Claude account.

- **Excel**: ask about cells and formulas, update a model without breaking it.
- **Word**: edits appear as **tracked changes**; Claude can answer comment threads. Handy for co-written proposals.
- **PowerPoint**: build or edit slides in your own template.
- **Outlook** (beta): triage your inbox and draft replies that wait for you to send them.

At UB, installing Office add-ins may also need UB IT approval.

## Keep it safe

- Claude **asks before sending, deleting or creating** anything. Read what it proposes before you approve. Better: ask for drafts and send them yourself.
- Your mailbox contains **other people's personal data**. Ask about specific threads or senders rather than "search all my email", and don't paste the results anywhere public.
- Emails can contain text written to manipulate AI assistants. Don't let Claude act automatically on instructions found inside an email.
- Disconnect services you no longer use: **Customize → Connectors → Disconnect**.

See also [Data and privacy](../getting-started/data-and-privacy.md).
