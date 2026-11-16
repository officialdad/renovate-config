# renovate-config

Shared Renovate preset for the officialdad org.

## What it does

- Extends `config:recommended` and pins GitHub Actions to full commit SHAs with version comments (`helpers:pinGitHubActionDigests`).
- Opens update PRs without waiting for a person to tick a box on the dashboard (`dependencyDashboardApproval: false`).
- Keeps Renovate auto-merge off (`automerge: false`); the ops bot merges green minor and patch PRs.
- Labels every PR `dependencies`, and adds `major` to major updates.
- Limits PR noise: at most 5 concurrent PRs and 2 per hour per repo.
- Groups GitHub Actions minor and patch updates into one PR per repo.

## Adopt it

Add this `renovate.json` to a repo:

```json
{
  "extends": ["github>officialdad/renovate-config"]
}
```
