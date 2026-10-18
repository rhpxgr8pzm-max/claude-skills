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
/plugin marketplace add <github-user>/claude-skills
/plugin install core@thomas-skills
```

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
