---
tags:
  - Admin
  - Connectors
  - Email
---

# Conference trip reimbursement from your email

!!! info "Illustrative example"
    This example was written by the site editors to show the workflow. It is not yet a real ICCUB experience. If you try it, [send us your version](../../contribute/index.md) and we will replace it.

| About this example | |
| --- | --- |
| **Author** | ICCUB Claude Guide editors |
| **Date** | 2026-10-06 |
| **Area** | Admin |
| **Tools used** | Gmail and Google Drive connectors (or Microsoft 365), Claude in Chrome (optional) |
| **Time saved** | About an hour per trip (estimate) |

## Goal

Back from a conference, gather everything needed for the travel reimbursement: registration receipt, flights, hotel, local transport, per diem dates. Then fill the department's expense sheet and draft the email to the administration, without digging through dozens of emails.

## What I did

1. **Connected the mailbox** once (see [Email, calendar and documents](../../using-claude/email-calendar.md)) and switched on the email and Drive connectors in a new chat.

2. **Gathered the documents:**

    > *I attended a conference in Lisbon from 29 June to 3 July 2026. Search my email for the registration receipt, flight bookings, hotel confirmation, and any other payment related to this trip. Make a table: date, item, supplier, amount, currency, payment method, and a link to the email. Flag anything missing.*

    It found five items and flagged that the hotel invoice was a booking confirmation, not an invoice.

3. **Filled the form.** Uploaded the department's expense template (Excel) and the list of rules:

    > *Fill this expense sheet with the items from the table. Use the per diem rules in the attached document for the travel days. Convert any non-euro amounts with the exchange rate on the payment date and say which rate you used.*

4. **Drafted the email:**

    > *Draft an email in Catalan to the department administration, attaching the filled sheet, listing the receipts, and asking for the missing hotel invoice procedure. Don't send it.*

5. **Checked everything** against the receipts, downloaded the attachments, and sent the email myself.

6. *(Optional)* For the hotel invoice, used [Claude in Chrome](../../using-claude/chrome.md) to log in to the hotel's booking site and find the invoice download page. I clicked "download" myself.

## Result

All receipts found, an expense sheet filled, and a draft email, in about 15 minutes instead of an hour and a half. One missing document was spotted before submitting rather than after.

## What to watch for

- **Amounts and dates**: check every number against the receipts. This is money.
- **Receipts vs. confirmations**: administration usually needs invoices. Ask Claude to flag the difference.
- **Attachments**: connectors can read attachments, but writing tools may not be able to attach files to emails. Attach them yourself.
- **Don't let it send.** Ask for drafts.
- **Personal data**: your mailbox has other people's data. Keep the search specific to the trip.
- **UB rules change**: give it the current rules document rather than relying on what it "knows".
