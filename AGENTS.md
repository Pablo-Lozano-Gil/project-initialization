# Repository Guidelines

## How to Use This Guide

- Start here for cross-project norms. The project is a monorepo with several components.
- Each component has an `AGENTS.md` file with specific guidelines (e.g., `api/AGENTS.md`, `ui/AGENTS.md`).
- Component docs override this file when guidance conflicts.

## Available Skills

Use these skills for detailed patterns on-demand:

### Generic Skills (Any Project)

| Skill | Description | URL |
| ------- | ----------- | ----- |
| `pytest` | Fixtures, mocking, markers, parametrize | [SKILL.md](.agent/skills/pytest/SKILL.md) |

### Project-Specific Skills

| Skill | Description | URL |
| ------- | ------------- | ----- |
| `skill-creator` | Create new AI agent skills | [SKILL.md](.agent/skills/skill-creator/SKILL.md) |
| `product-discovery` | Research and analyze product ideas | [SKILL.md](.agent/skills/product-discovery/SKILL.md) |

### Auto-invoke Skills

When performing these actions, ALWAYS invoke the corresponding skill FIRST:

| Action | Skill |
| -------- | ------- |
| Writing Python tests with pytest | `pytest` |
| Creating new AI agent skills | `skill-creator` |

---

## Project Overview

{Project-description}.

| Component | Location | Tech Stack |
| ----------- | ---------- | ------------ |
| SDK | `{project-name}/` | Python 3.12+, uv |
| API | `api/` | FastAPI, uv |
| UI | `ui/` | Astro.js, Tailwind 4 |

---

## Python Development

```bash
# Setup
uv init
uv sync --all-extras

# Code quality (using Ruff from Astral)
ruff check
ruff format
```

---

## Commit & Pull Request Guidelines

Follow conventional-commit style: `<type>[scope]: <description>`

**Types:** `feat`, `fix`, `docs`, `chore`, `perf`, `refactor`, `style`, `test`

Before creating a PR:

1. Complete checklist in `.github/pull_request_template.md`
2. Run all relevant tests and linters
3. Link screenshots for UI changes
