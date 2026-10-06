# Memphis Quotes — Chris Jeans Insurance Agency

A single-page, mobile-first quote request form for Chris Jeans Insurance Agency (Memphis, TN). Visitors pick the coverage they want (renters, auto, home/condo, life), leave their contact details, and the submission is posted to the agency's Google Form.

- Plain HTML/CSS/JS, no build step (`index.html`)
- Hosted on Netlify as a static site (`netlify.toml` publishes the repo root)
- Referral links: `/?ref=<partner-key>` shows a "Referred by" badge and prefills address/source (partners are configured in the `CONFIG` block at the top of `index.html`)

## Run locally

Open `index.html` in a browser, or run `netlify dev`.
