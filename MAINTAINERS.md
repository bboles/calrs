# Maintainers

calrs is maintained by a small group of people, with a single project lead and per-feature maintainers who own specific integrations they actively use. The lead reviews and merges all changes; provider maintainers are the first point of contact and the de-facto reviewer for changes touching their area.

## Project maintainer

- **Olivier Lambert** ([@olivierlambert](https://github.com/olivierlambert))
  Overall direction, releases, security review, code style. Final say on every merge.

## Provider maintainers

Each CalDAV provider integration is owned by someone who actually runs that provider in production. The owner verifies that PRs touching the provider keep it working, triages provider-specific bug reports, and is consulted when the project lead reviews changes that affect the integration.

Listing a maintainer here does **not** transfer commit rights, it sets the expectation of who reviews and signs off on changes for that area.

| Provider | Maintainer | Status |
|---|---|---|
| BlueMind | [@olivierlambert](https://github.com/olivierlambert) | Primary test target. |
| Nextcloud | _(seeking maintainer)_ | Used by some users; no dedicated owner. |
| Google Calendar | [@bboles](https://github.com/bboles) | OAuth2 path added in #99. |
| SOGo | _(seeking maintainer)_ | Not personally tested by the project lead. |
| Zimbra | _(seeking maintainer)_ | Not personally tested by the project lead. |
| Radicale | _(seeking maintainer)_ | Not personally tested by the project lead. |
| iCloud | _(seeking maintainer)_ | Not personally tested by the project lead. |
| Fastmail | _(seeking maintainer)_ | Not personally tested by the project lead. |

## Becoming a provider maintainer

If you actively use one of the providers above (or want to add a new one) and are willing to:

- Run a recent calrs build against your provider periodically.
- Respond to bug reports tagged with your provider in a reasonable timeframe.
- Review PRs that touch your provider's integration code.

…then open an issue or comment on an existing one and we'll add you here. You don't need to commit to anything formal beyond "I care that this keeps working."

## What happens if a provider has no maintainer

We don't promise that integrations without a dedicated maintainer keep working across releases. If a refactor breaks an unmaintained provider and no test catches it, the breakage may ship and only get fixed when someone who uses that provider files a bug. Provider maintainers exist to give those integrations a faster feedback loop.
