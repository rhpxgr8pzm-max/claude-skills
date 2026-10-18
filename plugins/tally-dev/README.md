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

Left out on purpose: ECC's JS/React/Node-focused skills (`coding-standards`,
`tdd-workflow`, `frontend-patterns`, `backend-patterns`, `e2e-testing`) and
Postgres-specific ones.

To refresh from upstream, re-copy the skill folders from ECC and bump `version`.
