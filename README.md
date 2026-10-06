# Lean on Jeans: quote request page

A single-page, mobile-first quote request page for Chris Jeans - State Farm Insurance Agent (Memphis, TN). Visitors can call or text the office, or choose the coverage they want and leave their contact details.

- Plain HTML/CSS/JS, no build step: `index.html` (quote page) and `privacy/index.html` (privacy policy)
- Hosted on **GitHub Pages** from the `main` branch, repo root: https://squeaky90.github.io/leanonjeans/
- Form submissions are posted to the agency's **Google Form**. A Google Apps Script ("Quote Lead Emails") attached to that form emails each lead to chris@leanonjeans.com.
- Google Analytics tag `G-CK6XMJN1K5`: `generate_lead` fires on a submitted form, `phone_call_click` on any Call/Text tap.
- Referral links: `/?ref=<partner-key>` prefills "How'd you hear about us?" (partners are in the `CONFIG` block at the top of `index.html`).

## Run locally

Open `index.html` in a browser, or run `python3 -m http.server` in this folder.
