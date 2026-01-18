---
name: skill-propagator
description: >
  Propagates skill metadata to AGENTS.md Auto-invoke sections.
  Trigger: When updating skill metadata (metadata.scope/metadata.auto_invoke), regenerating Auto-invoke tables, or running .agent/skills/skill-propagator/assets/propagate.sh (including --dry-run/--scope).
license: Apache-2.0
metadata:
  author: prowler-cloud & Pablo Lozano
  version: "1.0"
  scope: [root]
  auto_invoke:
    - "After creating/modifying a skill"
    - "Regenerate AGENTS.md Auto-invoke tables (propagate.sh)"
    - "Troubleshoot why a skill is missing from AGENTS.md auto-invoke"
allowed-tools: Read, Edit, Write, Glob, Grep, Bash
---
# Skill Propagator

## Purpose

Keeps AGENTS.md Auto-invoke sections in sync with skill metadata. When you create or modify a skill, run the propagate script to automatically update all affected AGENTS.md files.

## Required Skill Metadata

Each skill that should appear in Auto-invoke sections needs these fields in `metadata`.

`auto_invoke` can be either a single string **or** a list of actions:

```yaml
metadata:
  author: Pablo Lozano
  version: "1.0"
  scope: [ui]                                    # Which AGENTS.md: ui, api, sdk, root

  # Option A: single action
  auto_invoke: "Creating/modifying components"

  # Option B: multiple actions
  # auto_invoke:
  #   - "Creating/modifying components"
  #   - "Refactoring component folder placement"
```

### Scope Values

| Scope | Updates |
| ------- | --------- |
| `root` | `AGENTS.md` (repo root) |
| `ui` | `ui/AGENTS.md` |
| `api` | `api/AGENTS.md` |
| `sdk` | `{project-name}/AGENTS.md` |
| `mcp_server` | `mcp_server/AGENTS.md` |

Skills can have multiple scopes: `scope: [ui, api]`

---

## Usage

### After Creating/Modifying a Skill

```bash
.agents/skills/skill-propagator/assets/propagate.sh
```

### What It Does

1. Reads all `.agent/skills/*/SKILL.md` files
2. Extracts `metadata.scope` and `metadata.auto_invoke`
3. Generates Auto-invoke tables for each AGENTS.md
4. Updates the `### Auto-invoke Skills` section in each file

---

## Example

Given this skill metadata:

```yaml
# .agent/skills/astro-ui/SKILL.md
metadata:
  author: Pablo Lozano
  version: "1.0"
  scope: [ui]
  auto_invoke: "Creating/modifying ASTRO components"
```

The sync script generates in `ui/AGENTS.md`:

```markdown
### Auto-invoke Skills

When performing these actions, ALWAYS invoke the corresponding skill FIRST:

| Action | Skill |
| -------- | ------- |
| Creating/modifying ASTRO components | `astro-ui` |
```

---

## Commands

```bash
# Sync all AGENTS.md files
./.agent/skills/skill-propagator/assets/propagate.sh

# Dry run (show what would change)
./.agent/skills/skill-propagator/assets/propagate.sh --dry-run

# Sync specific scope only
./.agent/skills/skill-propagator/assets/propagate.sh --scope ui
```

---

## Checklist After Modifying Skills

- [ ] Added `metadata.scope` to new/modified skill
- [ ] Added `metadata.auto_invoke` with action description
- [ ] Ran `./.agent/skills/skill-propagator/assets/propagate.sh`
- [ ] Verified AGENTS.md files updated correctly
