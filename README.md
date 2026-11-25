# Outreach Desk

A single-page app for brand partnership outreach on behalf of creators. It runs as a Claude artifact and uses the viewer's Gmail and monday.com connectors.

## What it does

- **Generate new brands** for a creator, with a one-line reason each.
- **Find contacts** on LinkedIn (through the Claude desktop app's browser pane) and guess each person's email from the company's address format.
- **Draft emails** two at a time per brand (the waterfall: 2 emails, then a 3 to 4 day gap, then 2 more), saved as Gmail drafts with the logo signature and a link to the creator's TikTok.
- **Review and send**: shows the batch, sends only after you press Approve, with per-brand and daily limits.
- **Watches Gmail** for sends, replies, bounces and emails from anyone else at the company, and pauses or closes a brand accordingly.
- **Update monday.com** rows and contact subitems.

## Files

- `outreach-desk.html` — the whole app. It is published as a Claude artifact; it does not run as a normal web page because it relies on the artifact runtime (`window.claude`) for its database, Claude calls and connectors.
- `docs/hourly-gmail-check.md` — the prompt for the optional hourly background Gmail check (a Claude scheduled task). It is currently switched off.

## Data

Creators, brands, contacts, settings and the signature logo live in the artifact's own database, not in this repository.
