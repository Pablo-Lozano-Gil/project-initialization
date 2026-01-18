---
description: Automate Skill Documentation Propagation by taking all the skills in the .agent/skills folder and update the README.md of the folder and all the relevant AGENTS.md files of the repository
---

Skills source: .agent/skills/*/SKILL.md
Targets: .agent/skills/README.md and **/AGENTS.md

Logic:

- Iterate through the .agent/skills directory.
- Parse metadata (name, description, inputs) from each skill file.
- Action A: Update the .agent/skills/README.md to serve as a central catalog of available tools.
- Action B: Search the repository for AGENTS.md files. For each agent found, cross-reference its configuration to determine which skills it uses, and update its documentation file to match the latest definitions in the source folder.
