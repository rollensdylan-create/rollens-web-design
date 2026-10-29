# Rollens Web Design / WebForge

Source snapshot: 30 October 2026 (Australia/Melbourne).

The current application source is in `webforge/` inside `rollens-web-design-2026-10-30.zip`.

Includes the redesigned prompt-led homepage, self-service customer accounts and editor, Starter/Plus draft editing locks and Pro ongoing editing, recurring Stripe checkout and webhooks, paid publication, verified custom domains and automatic HTTPS, improved automated demo generation and quality checks, private operator dashboard, Anakin primary business discovery, tests and VPS deployment examples.

Prices: Starter A$19.99/month, Plus A$33/month, Pro A$99/month. Starter/Plus each support one site; Pro supports multiple sites.

## Run locally

1. Extract the ZIP and enter `webforge/`.
2. Install Node.js 24 and pnpm, then run `pnpm install --frozen-lockfile`.
3. Run `pnpm exec playwright install chromium`.
4. Review `.env.example` and configure private credentials locally or in the private dashboard's encrypted Connections store.
5. Run `pnpm build`, then `pnpm start` and `pnpm worker` in separate terminals.
6. Open http://127.0.0.1:4333. The operator dashboard must stay private in production.

## Deployment and verification

VPS examples and feature instructions are under `webforge/deploy/vps/`, including custom-domain and Anakin integration notes. The source was built and tested during deployment on 28 October; 61 server tests passed. This upload does not redeploy the live service. Earlier validation documents inside the application folder are historical recovery records.

Anakin is the current primary discovery provider. Existing schedules and daily scan caps are preserved. Campaign email sending remains disabled; discovered contact information does not establish marketing permission.

This is a source backup, not a database backup. No customer records, uploads, production SQLite database, passwords, service API keys, encrypted connection files, generated builds, node_modules or browser sessions are included. Re-enter credentials privately when restoring. SHA256SUMS verifies the source ZIP; SOURCE_MANIFEST.json inside the ZIP lists every source file checksum.
