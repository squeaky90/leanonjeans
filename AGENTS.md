# AGENTS.md

- Static site, no framework, no build. Hosted on GitHub Pages from `main` / repo root (`.nojekyll` disables Jekyll). `netlify.toml` is kept only so the repo can still deploy on Netlify; Netlify Forms are not used.
- All settings (phone, Google Form ID and `entry.*` field IDs, analytics/Ads IDs, referral partners) are in the `CONFIG` object at the top of `index.html`. Edit there, not in the markup.
- Submissions POST to the Google Form (`formResponse`, `no-cors`). Choice values must match the form's options exactly (e.g. `Home/Condo`). Questions still marked required in the Google Form get fallback values in the submit handler; keep those in place unless the form is changed.
- Lead emails come from the Apps Script trigger on the Google Form, not from this page.
- Analytics events must fire only on user action (one `generate_lead` per successful submission, one `phone_call_click` per tel:/sms: tap), never on page load.
- Keep the State Farm disclosures, license numbers, TCPA consent wording and privacy link intact.
