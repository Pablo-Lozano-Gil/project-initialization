# Project Initialization Template

> **AI-Powered Development Starter Kit** - A battle-tested project initialization repository designed to accelerate development with pre-configured AI agents, skills, and best practices for modern software development.

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![OpenCode Compatible](https://img.shields.io/badge/OpenCode-Compatible-blue)](https://opencode.ai)
[![Agent Skills](https://img.shields.io/badge/Agent%20Skills-Enabled-green)](https://agentskills.io)

## 🎯 Purpose

This repository serves as a **starting point** for new projects, providing:

- **Pre-configured AI agents** with specialized personas (Senior Architect, Research Consultant)
- **Reusable agent skills** following the [Agent Skills open standard](https://agentskills.io)
- **Development workflows** and automation scripts
- **Best practices** for AI-assisted development
- **Ready-to-use configurations** for popular AI coding assistants (Antigravity, Claude Code, OpenCode, Cursor...)

## ✨ Key Features

### 🤖 AI Agent Definitions

Pre-configured AI personas for different development contexts:

- **Gentleman** - Senior Architect mentor (Google Developer Expert, Microsoft MVP)
  - Passionate teacher focused on helping you learn and grow
  - Expertise in modern development practices and architecture
  - Warm, collaborative tone with technical depth

- **Researcher** - European Commission Research Consultant
  - Specializes in Horizon Europe projects (Cluster 5: Climate, Energy, Mobility)
  - Expert in transport safety and biomechanics
  - Proposal review and improvement specialist

### 🧠 Agent Skills Library

Following the [Agent Skills open standard](https://agentskills.io), this repository includes:

#### Generic Skills (Reusable Across Projects)

- **pytest** - Python testing patterns (fixtures, mocking, markers, parametrize)

#### Meta Skills (Skill Management)

- **skill-creator** - Create new AI agent skills following best practices
- **skill-propagator** - Automate skill documentation propagation

All skills are automatically discovered by AI assistants and provide:

- Critical rules and conventions
- Code patterns and best practices
- Project-specific workflows
- References to detailed documentation

### 📋 Project Structure

```text
.
├── .agent/                      # AI agent configuration
│   ├── skills/                  # Agent Skills library
│   │   ├── pytest/             # Python testing patterns
│   │   ├── skill-creator/      # Skill creation tool
│   │   ├── skill-propagator/   # Skill documentation sync
│   │   ├── setup.sh            # Skills setup script
│   │   └── README.md           # Skills documentation
│   └── workflows/              # Automated workflows
│       └── skill-propagation.md
│
├── opencode_agent_definitions/  # Custom agent personas
│   ├── gentleman.md            # Senior Architect persona
│   ├── researcher.md           # Research Consultant persona
│   └── security_auditor.md     # Security expert persona
│
├── themes/                      # UI themes for agents
│   └── gentleman.json          # Gentleman theme
│
├── .github/                     # GitHub configuration
│   └── pull_request_template.md
│
├── AGENTS.md                    # AI agent guidelines
├── opencode.json                # OpenCode configuration
└── README.md                    # This file
```

### 🛠️ Development Setup

The repository includes configuration for:

- **Python Development**: Using `uv` for package management, Ruff for linting
- **Code Quality**: Pre-configured linters and formatters
- **CLI Tools**: Modern alternatives (bat, rg, fd, sd, eza)
- **Conventional Commits**: Standardized commit messages

## 🚀 Quick Start

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/project_initialization.git
cd project_initialization
```

### 2. Setup AI Agent Skills

Run the setup script to configure skills for all supported AI coding assistants:

```bash
.agent/skills/setup.sh
```

This creates symlinks for:

- Claude Code / OpenCode (`.claude/skills/`)
- Codex (`.codex/skills/`)
- GitHub Copilot (`.github/skills/`)
- Gemini CLI (`.gemini/skills/`)

### 3. Configure Your AI Assistant

The repository comes with pre-configured `opencode.json` for OpenCode:

```json
{
  "default_agent": "gentleman",
  "theme": "gentleman",
  "autoupdate": true,
  "mcp": {
    "context7": {
      "type": "remote",
      "url": "https://mcp.context7.com/mcp",
      "enabled": true
    }
  }
}
```

### 4. Start Developing

Your AI assistant now has access to:

- Specialized agent personas
- Domain-specific skills
- Best practices and patterns
- Automated workflows

## 📚 Usage

### Using Agent Skills

Skills are automatically discovered. To manually load a skill during a session:

```text
Read .agent/skills/pytest/SKILL.md
```

### Creating New Skills

Use the skill-creator skill for guidance:

```text
Read .agent/skills/skill-creator/SKILL.md
```

**Quick Checklist:**

1. Create directory: `.agent/skills/{skill-name}/`
2. Add `SKILL.md` with required frontmatter
3. Add `metadata.scope` and `metadata.auto_invoke` fields
4. Keep content concise (under 500 lines)
5. Reference existing docs instead of duplicating
6. Run skill propagation workflow

### Running Workflows

Use the skill propagation workflow to update documentation:

```text
# Run the skill propagation workflow
# This updates README.md and AGENTS.md files with skill metadata
```

## 🔧 Customization

### Add Your Own Agent Personas

Create a new file in `opencode_agent_definitions/`:

```markdown
# Your Agent Name

**Description of your agent...**

## Core Principles
- Principle 1
- Principle 2

## Expertise
- Area 1
- Area 2
```

Then update `opencode.json` to include your agent.

### Create Project-Specific Skills

1. Use the `skill-creator` skill
2. Add your skill to `.agent/skills/`
3. Run skill propagation to update docs
4. Restart your AI assistant

## 🎓 Philosophy

This repository is built on core development principles:

- **CONCEPTS > CODE**: Understand before coding
- **AI IS A TOOL**: You direct, AI executes (Tony Stark/Jarvis model)
- **FOUNDATIONS FIRST**: Master fundamentals before frameworks
- **COLLABORATIVE LEARNING**: AI as a mentor, not an interrogator

## 🤝 Contributing

Contributions are welcome! Areas for contribution:

- **New Skills**: Add domain-specific patterns and conventions
- **Agent Personas**: Create specialized AI personas for different roles
- **Workflows**: Automate common development tasks
- **Documentation**: Improve setup guides and examples

### Commit Guidelines

Follow conventional-commit style: `<type>[scope]: <description>`

**Types:** `feat`, `fix`, `docs`, `chore`, `perf`, `refactor`, `style`, `test`

## 📖 Resources

- [Agent Skills Standard](https://agentskills.io) - Open standard specification
- [OpenCode Documentation](https://opencode.ai)
- [Claude Code Best Practices](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/best-practices)
- [Conventional Commits](https://www.conventionalcommits.org/)

## 💡 Use Cases

Perfect for:

- **Starting new projects** with AI-assisted development
- **Standardizing team workflows** across projects
- **Teaching AI best practices** to development teams
- **Research projects** requiring proposal review and improvement
- **Multi-agent development** with specialized AI personas

## 📝 License

Apache License 2.0 - See [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Built with [Agent Skills](https://agentskills.io) open standard
- Compatible with [OpenCode](https://opencode.ai)
- Inspired by modern AI-assisted development practices and [Prowler](https://github.com/prowler-cloud/prowler/tree/master)
- Community-driven skill development

---

**Ready to accelerate your development?** Clone this repository and start building with AI-powered assistance! 🚀
