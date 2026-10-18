# claude-skills

Thomas's personal Claude Code plugin marketplace.

## Layout

```
.claude-plugin/marketplace.json        # marketplace catalog (lists the plugins)
plugins/<plugin>/.claude-plugin/plugin.json
plugins/<plugin>/skills/<skill>/SKILL.md
```

Group skills into plugins by theme (e.g. `core`, `excel`, `tax`) so each project
installs only what it needs.

## Install (inside Claude Code)

```
/plugin marketplace add rhpxgr8pzm-max/claude-skills
/plugin install core@thomas-skills
/plugin install repomix-mcp@thomas-skills
/plugin install repomix-commands@thomas-skills
/plugin install repomix-explorer@thomas-skills
```

## Included plugins

| Plugin | Source | What it does |
| --- | --- | --- |
| `core` | this repo | General-purpose skills |
| `repomix-mcp` | yamadashy/repomix | MCP server that packs repos into one AI-friendly file (install first) |
| `repomix-commands` | yamadashy/repomix | `/repomix-commands:pack-local`, `pack-remote` |
| `repomix-explorer` | yamadashy/repomix | Codebase analysis agent |
| `tally-dev` | this repo (curated from affaan-m/ECC) | 8 Python/testing/security/LLM skills for Tally. Install per project |

## Add a third-party plugin

Point an entry at the other repo instead of copying it, so upstream updates flow through:

```json
{ "name": "x", "source": { "source": "git-subdir", "url": "owner/repo", "path": "path/to/plugin" } }
```

Use `"source": "github", "repo": "owner/repo"` when the plugin is the whole repo.
Add `"ref"` or `"sha"` to pin a version.

Or browse with `/plugin` → Discover. After pushing changes:

```
/plugin marketplace update thomas-skills
```

## Add a skill

1. Copy `plugins/core/skills/skill-template` to a new folder.
2. Edit `SKILL.md` — the `description` decides when Claude uses it.
3. Bump `version` in `plugin.json` and `marketplace.json`, commit, push.

## Add a plugin

1. Create `plugins/<name>/.claude-plugin/plugin.json` and `plugins/<name>/skills/`.
2. Add an entry to `.claude-plugin/marketplace.json`.

## Local testing

```
claude plugin validate .
claude --plugin-dir ./plugins/core
```
