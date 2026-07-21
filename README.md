# Spark Codex Marketplace

Curated [Codex](https://developers.openai.com/codex) plugin marketplace for [Spark](https://sparkmailapp.com). Add this marketplace to Codex to browse and install Spark plugins.

## Requirements

- macOS or Windows with a recent build of [Spark Desktop](https://sparkmailapp.com), signed in to at least one account.
- Spark CLI enabled: in Spark, go to **Settings → AI Agents → Spark CLI Setup** and follow the prompts.
- Per-account access levels - `read-only`, `triage` (everything in read-only plus drafts, comments, and email/contact actions), or `send` (everything in triage plus sending mail and calendar invitations) - configured in **Settings → AI Agents -> Spark CLI Access**. Recipes and personas declare the level they need; running one against an account with insufficient access returns an error explaining how to upgrade.

## Adding the marketplace

```bash
codex plugin marketplace add readdle/spark-codex-marketplace
```

Or via the Codex GUI: **Plugins → Manage → Add marketplace**, with `git@github.com:readdle/spark-codex-marketplace.git` as the source.

## Plugins

| Plugin | Description |
|--------|-------------|
| [spark-cli-skills](https://github.com/readdle/spark-cli-skills) | AI agent skills for the Spark CLI - email, calendar, contacts, teams, and meetings workflows |

## Adding a new plugin

Each plugin entry lives under `plugins[]` in [`.agents/plugins/marketplace.json`](.agents/plugins/marketplace.json). For Git-backed plugins at the repository root, use `"source": "url"`; for plugins in a subdirectory, use `"source": "git-subdir"` with a `path` field. See the [Codex docs](https://developers.openai.com/codex/plugins/build) for the full schema.

## License

[MIT](LICENSE)
