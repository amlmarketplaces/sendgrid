# amlmarketplaces/sendgrid

Claude Code marketplace federating all `@amlplugins/sendgrid-*` plugins.

## Install

Add to your project's `.claude/settings.json`:

```json
{
  "extraKnownMarketplaces": {
    "aml-sendgrid": {
      "source": { "source": "github", "repo": "amlmarketplaces/sendgrid" }
    }
  },
  "enabledPlugins": {
      "sendgrid-domain-authentication@aml-sendgrid": true,
      "sendgrid-event-webhook@aml-sendgrid": true,
      "sendgrid-inbound-parse@aml-sendgrid": true,
      "sendgrid-mail@aml-sendgrid": true,
      "sendgrid-marketing@aml-sendgrid": true
    }
}
```

Then launch Claude Code in the project. The marketplace is fetched from `amlmarketplaces/sendgrid`, cached under `~/.claude/plugins/cache/aml-sendgrid/`, and each enabled plugin is loaded from its `amlplugins` source repo.

## Plugins (6 total)

- `sendgrid-domain-authentication` — [@amlplugins/sendgrid-domain-authentication](https://github.com/amlplugins/sendgrid-domain-authentication)
- `sendgrid-event-webhook` — [@amlplugins/sendgrid-event-webhook](https://github.com/amlplugins/sendgrid-event-webhook)
- `sendgrid-inbound-parse` — [@amlplugins/sendgrid-inbound-parse](https://github.com/amlplugins/sendgrid-inbound-parse)
- `sendgrid-mail` — [@amlplugins/sendgrid-mail](https://github.com/amlplugins/sendgrid-mail)
- `sendgrid-marketing` — [@amlplugins/sendgrid-marketing](https://github.com/amlplugins/sendgrid-marketing)
- `sendgrid-suppression` — [@amlplugins/sendgrid-suppression](https://github.com/amlplugins/sendgrid-suppression)

## Related

- npm packages: `@amlplugins/sendgrid-*` published to GitHub Packages (`https://npm.pkg.github.com`).
- Aggregating parent: [`amlmarketplaces/aml`](https://github.com/amlmarketplaces/aml) — federates every `@amlplugins/*` plugin under a single marketplace.
- AML topology: see `.claude/rules/definitions/ageni.md` § "GitHub Topology" — this repository is a Tier-4 HUB-INSTANCE under the `amlmarketplaces/` Tier-3 HUB-ORGANIZATION.

> Built by `.claude/skills/aml/metateam/marketplace/test/cross-org-amlmarketplaces-batch.mjs`.
