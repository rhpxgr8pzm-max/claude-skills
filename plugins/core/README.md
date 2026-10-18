# core

General-purpose skills and commands for every project.

| Item | Type | What it does |
| --- | --- | --- |
| `skill-template` | skill | Starting point for new skills |
| `/core:save-session` | command | Saves the session's state to `~/.claude/session-data/` so work can resume later |
| `/core:resume-session` | command | Loads the latest saved session (or one by date) and continues |

The two session commands are copied unchanged from
[affaan-m/ECC](https://github.com/affaan-m/ECC) at commit `76aaa77`
(MIT licence, see `LICENSE-ECC`).

Not taken from ECC: `checkpoint` (relies on ECC's `/verify`), `strategic-compact`
and `skill-health` (rely on ECC's Node scripts and hooks), `context-budget`
(Claude Code's `/context` covers it), `skill-create` (Anthropic's `skill-creator`
does this better).
