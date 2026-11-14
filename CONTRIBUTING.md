# Contributing

Thank you for your interest in contributing to this project! 🎉

This repository is a catalog of **Agent Skills** for AI coding assistants (GitHub Copilot, Claude Code, Gemini CLI, Google Antigravity). Contributions are welcome in the form of new skills, improvements to existing ones, bug fixes, and documentation.

---

## Table of Contents

- [Contributing](#contributing)
  - [Table of Contents](#table-of-contents)
  - [Code of Conduct](#code-of-conduct)
  - [How to Contribute](#how-to-contribute)
  - [Creating a New Skill](#creating-a-new-skill)
    - [Directory Structure](#directory-structure)
    - [`SKILL.md` Required Format](#skillmd-required-format)
    - [Skill Naming Guidelines](#skill-naming-guidelines)
    - [Skill Quality Checklist](#skill-quality-checklist)
  - [Improving an Existing Skill](#improving-an-existing-skill)
  - [Pull Request Guidelines](#pull-request-guidelines)
  - [Commit Message Convention](#commit-message-convention)
  - [Questions?](#questions)

---

## Code of Conduct

This project is licensed under the [Apache License 2.0](LICENSE). By contributing, you agree that your contributions will be licensed under the same license.

---

## How to Contribute

1. **Fork** the repository and create a branch from `main`.
2. Make your changes following the guidelines below.
3. Open a **Pull Request** with a clear title and description.
4. Wait for review — feedback will be provided within a few days.

---

## Creating a New Skill

Each skill lives in its own directory under `skills/` and must contain at least a `SKILL.md` file.

### Directory Structure

```text
skills/
└── your-skill-name/
    ├── SKILL.md            ← required
    ├── templates/          ← optional: output templates
    └── references/         ← optional: reference documentation
```

### `SKILL.md` Required Format

```markdown
---
name: your-skill-name
description: >-
  One or two sentences describing what this skill does and when to use it.
  Include what it does NOT do (routing boundary).
---

# Skill Title

## Outcome

What the agent produces or decides after running this skill.

## Routing

**Use when:** ...

**Do not use when:** ...

## Required context

- Item 1
- Item 2

## Non-negotiable operating rules

1. Rule one
2. Rule two
```

### Skill Naming Guidelines

- Use `kebab-case` for directory and skill names.
- Names should describe **what the skill does**, not the technology (e.g., `evidence-driven-debugger`, not `debugger-csharp`).
- Keep names concise — ideally 2–4 words.

### Skill Quality Checklist

Before submitting a new skill, verify:

- [ ] The `SKILL.md` YAML frontmatter is valid and complete.
- [ ] The `description` field clearly states the purpose and boundary.
- [ ] The **Routing** section defines clear `Use when` and `Do not use when` rules.
- [ ] The skill does not duplicate an existing one — check the [catalog](README.md) first.
- [ ] The skill has been tested with at least one AI agent (Copilot, Claude, Gemini, or Antigravity).
- [ ] The root `README.md`, `skills/README.md`, and `CHANGELOG.md` are updated.

---

## Improving an Existing Skill

- For **typos or small fixes**, open a PR directly.
- For **behavior changes** (routing rules, output format, required context), open an issue first to discuss the change.
- Avoid changing a skill's `name` field — it may break existing installations.

---

## Pull Request Guidelines

- **Title**: Follow the [commit convention](#commit-message-convention) below.
- **Description**: Explain *what* changed and *why*. Link related issues with `Closes #N`.
- **Scope**: Keep PRs focused — one skill or one concern per PR.
- **Tests**: If you add a skill, include at least one example prompt → expected output in the PR description.

---

## Commit Message Convention

This project uses [Conventional Commits](https://www.conventionalcommits.org/):

```
<type>: <short summary>
```

| Type       | When to use                                              |
| :--------- | :------------------------------------------------------- |
| `feat`     | New skill or new capability in an existing skill         |
| `fix`      | Bug fix or correction in skill logic/routing             |
| `docs`     | README, CHANGELOG, or documentation-only changes         |
| `refactor` | Restructuring skill content without behavior change      |
| `chore`    | Scripts, CI, install tooling, or repository housekeeping |

**Examples:**

```
feat: add observability-advisor skill
fix: correct routing boundary in evidence-driven-debugger
docs: update README with new skill catalog table
chore: add Apache 2.0 license and CONTRIBUTING.md
```

---

## Questions?

Open a [GitHub Discussion](https://github.com/Marcus-V-Freitas/MVFC.AgentSkills/discussions) or an [Issue](https://github.com/Marcus-V-Freitas/MVFC.AgentSkills/issues) — happy to help!
