# tally-dev

Skills for developing Tally, copied unchanged from
[affaan-m/ECC](https://github.com/affaan-m/ECC) at commit `76aaa77`
(MIT licence, see `LICENSE-ECC`). No ECC hooks or agents are included.

| Skill | Why it's here |
| --- | --- |
| `python-patterns` | Idiomatic Python, type hints, project structure |
| `python-testing` | pytest, fixtures, mocking, TDD with Python |
| `error-handling` | Robust errors and user-facing messages (e.g. bad CSV imports) |
| `security-review` | Input handling, secrets (API keys), sensitive financial data |
| `api-design` | Designing the Flask routes / JSON endpoints |
| `regex-vs-llm-structured-text` | Rules-first parsing with LLM fallback: bank CSVs and transaction categorization |
| `cost-aware-llm-pipeline` | Keeping AI categorization cheap: model routing, caching, budgets |
| `verification-loop` | Build/lint/test/diff check before calling work done |
| `make-interfaces-feel-better` | UI polish: spacing, typography, borders, states, motion |
| `design-system` | Extract and keep consistent design tokens for the dark Notion-style UI |
| `accessibility` | WCAG 2.2 AA: contrast, focus, labels, keyboard use |
| `browser-qa` | Browser smoke tests of the running app (localhost:5000): console errors, forms, breakpoints, a11y |
| `architecture-decision-records` | Record design decisions as ADRs in `docs/adr/` |

## Agents

| Agent | Role |
| --- | --- |
| `python-reviewer` | Reviews Python changes: idioms, types, security, performance |
| `security-reviewer` | Flags secrets, unsafe input handling, injection risks |
| `silent-failure-hunter` | Finds swallowed errors and bad fallbacks (e.g. skipped import rows) |
| `code-simplifier` | Simplifies recently changed code without changing behaviour |
| `planner` | Plans larger features and refactors before coding (read-only) |

Agents not taken: `code-reviewer` (JS/TS-heavy, overlaps `python-reviewer`) and
`database-reviewer` (PostgreSQL-specific).

Left out on purpose: ECC's JS/React/Node-focused skills (`coding-standards`,
`tdd-workflow`, `frontend-patterns`, `backend-patterns`, `e2e-testing`,
`frontend-a11y`), Postgres-specific ones, and `finance-billing-ops` (SaaS billing,
not household finance). For bold visual direction, ECC itself recommends
Anthropic's `frontend-design` skill (anthropics/skills) over its own.

To refresh from upstream, re-copy the skill folders from ECC and bump `version`.
