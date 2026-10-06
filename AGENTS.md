# AGENTS.md

- Static site: everything lives in `index.html`; no framework, no build. `netlify.toml` publishes `.`.
- All agency settings (name, phone, address, notification email, optional fields, referral partners) are in the `CONFIG` object at the top of `index.html` — edit there, not in the markup.
- Submissions use Netlify Forms with the static form name `quote-request`; there is no custom backend. Inputs whose `CONFIG.optionalFields` entry is false are hidden and disabled.
- Email notifications are configured in Netlify, not by browser JavaScript. Keep the Netlify submission notification recipient synchronized with `CONFIG.notificationEmail` when changing it; editing that value alone does not change delivery.
- Keep all submitted field names in the static HTML so Netlify detects them on deploy. Run `node /opt/buildhome/.agents/skills/netlify-forms/scripts/enable.cjs` after implementing Netlify Forms.
