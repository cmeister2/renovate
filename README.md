# Renovate presets

Use the yayornay preset in a repository's Renovate configuration:

```json
{
  "extends": ["github>cmeister2/renovate:yayornay"]
}
```

It adds the `ai-triage` label while preserving existing labels. It keeps the
default preset's best practices, grouping, automerge and semantic commit settings.
Automatic assignees and review requests are cleared so yayornay can request human
review when needed.

The preset requests a three-day minimum release age. Updates with a release
timestamp wait until that age has passed; updates without a timestamp remain
eligible. Renovate delegates lockfile maintenance to package managers, so this
does not guarantee that every resolved transitive dependency is three days old.
See [Renovate's minimum release age documentation](https://docs.renovatebot.com/key-concepts/minimum-release-age/)
for datasource and package-manager support.

The existing `github>cmeister2/renovate` preset retains its assignment and review
settings. Use the named yayornay preset instead when opting into bot triage.
