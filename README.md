# commands

**Catalog of standalone Claude Code slash commands used across the FlexNetOS meta workspace.**

A FlexNetOS hub: `registry.json` is the single source of truth, `scripts/validate.py`
keeps it consistent (CI-enforced), and this README mirrors it. Follows the
[Hub Standard](https://github.com/FlexNetOS/template_hub/blob/master/docs/hub-standard.md).

Repo is named `commands` (not commands_hub) per the workspace .meta.yaml.

## Scope

In scope: standalone, reusable Claude Code slash commands (the `commands/*.md` format).

Out of scope: commands bundled inside a plugin → [`plugin_hub`](https://github.com/FlexNetOS/plugin_hub);
non-command prompts → [`prompt_hub`](https://github.com/FlexNetOS/prompt_hub).

## Catalog

_No entries yet — v0.1.0._

| Command | Category | Args | Status | Doc |
|---------|----------|------|--------|-----|
| _(none)_ | | | | |

## Entry shape

Each `commands[]` entry in [`registry.json`](registry.json) looks like:

```json
{
  "id": "code-review",
  "displayName": "/code-review",
  "category": "review",
  "status": "stable",
  "summary": "Reviews the current diff for correctness and reuse/simplification at a chosen effort level; can post inline PR comments.",
  "tags": ["review", "pr"],
  "commandName": "code-review",
  "argsHint": "[low|medium|high] [--comment|--fix]",
  "model": "opus",
  "allowedTools": ["Bash", "Read", "Edit"],
  "scriptPath": "entries/code-review.md",
  "doc": "entries/code-review.md",
  "snippet": "snippets/code-review.command.md"
}
```

Full field reference: [`registry.schema.json`](registry.schema.json).

## Adding a command

Add an entry to `registry.json`, create `entries/<id>.md` (and a
`snippets/<id>.command.md` command file if useful), add a Catalog row, then run
`python3 scripts/validate.py`. See the
[Hub Standard](https://github.com/FlexNetOS/template_hub/blob/master/docs/hub-standard.md).
