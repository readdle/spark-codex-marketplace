# Spark Codex Marketplace

Curated [Codex](https://developers.openai.com/codex) plugin marketplace for [Spark](https://sparkmailapp.com). Add this marketplace to Codex to browse and install Spark plugins.

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
