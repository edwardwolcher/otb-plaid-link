# otb-plaid-link

Temporary, internal OTB tool: a single static page that runs **Plaid Link** and handles the
**OAuth redirect** for connecting On the Boards' bank accounts (Columbia checking is an OAuth
institution and requires a registered HTTPS `redirect_uri`).

- No secrets here. The short-lived `link_token` is passed at runtime via `?link_token=…`; the page
  returns a single-use `public_token` to paste back for server-side exchange.
- Registered in the Plaid dashboard as an Allowed redirect URI.
- **Stopgap.** This will be folded into the OTB automation app; see the `plaid-bank-feeds` skill.
