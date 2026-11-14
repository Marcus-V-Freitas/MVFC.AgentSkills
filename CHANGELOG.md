# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [2.1.0] - 2026-11-14

### Added

- **`SECURITY.md`** — Security policy covering supported versions, vulnerability reporting channels, response timeline, scope, and out-of-scope items.

### Changed

- Repository renamed from **`dotnet-functional-use-case-spec`** to **`MVFC.AgentSkills`** to reflect its expanded scope as a general-purpose AI agent skill library. GitHub redirects from the old name automatically.

## [2.0.0] - 2026-11-14

### Added

- **`behavior-preserving-refactor`** — Refactors existing code while preserving externally observable behavior. Covers simplification, decomposition, duplication removal, and maintainability improvements without introducing intentional behavior changes.
- **`change-impact-analyzer`** — Maps direct and transitive effects of proposed or applied code changes across contracts, callers, behavior, data, tests, deployment, and operations. Recommended before risky edits, releases, or pull requests.
- **`codebase-explorer`** — Orients and navigates unfamiliar repositories by explaining entrypoints, modules, dependencies, state flow, key workflows, and where to make a change. Ideal for onboarding and targeted code navigation.
- **`code-review-specialist`** — Reviews code changes and pull requests for demonstrable correctness, reliability, security, maintainability, and regression risks. Focuses on actionable defects without burying findings under style preferences.
- **`evidence-driven-debugger`** — Diagnoses reproducible software defects or unexpected runtime behavior using evidence, falsifiable hypotheses, targeted experiments, and regression tests. Covers crashes, wrong outputs, intermittent bugs, hangs, and unexplained failures.
- **`implementation-plan-reviewer`** — Reviews an existing technical implementation plan for feasibility, missing prerequisites, ordering, validation, risk, and rollback before significant work begins.
- **`migration-strategy-planner`** — Plans safe transitions between frameworks, data schemas, components, libraries, services, or deployment topologies with compatibility, rollout, verification, and rollback strategies.
- **`observability-advisor`** — Assesses and improves operational visibility through appropriate logs, metrics, traces, health signals, and diagnostic context. Ensures critical operations and failures can be diagnosed from production-safe signals.
- **`performance-investigator`** — Investigates measurable latency, throughput, CPU, memory, I/O, or scalability regressions using baselines and controlled experiments. Locates the dominant bottleneck and quantifies its impact.
- **`root-cause-investigator`** — Investigates incidents or recurring failures by constructing an evidence-based timeline, causal explanations, contributing factors, and prevention actions. Designed for postmortems and system-level failure analysis.
- **`security-reviewer`** — Reviews code, configuration, and system flows for defensible security risks, trust-boundary violations, authorization gaps, injection, sensitive-data exposure, and unsafe defaults.
- **`test-quality-auditor`** — Audits existing tests for the behaviors they truly prove, oracle quality, isolation, determinism, useful failure sensitivity, and missing risk coverage. Distinguishes test count from tested behavior and false confidence.

### Changed

- Root `README.md` updated with the full 20-skill catalog, expanded workflow, and updated repository structure tree.
- `skills/README.md` updated with all new skills and revised recommended workflow.

## [1.1.0] - 2026-10-24

### Added

- Cross-platform installation scripts (`install.ps1` and `install.sh`) with support for GitHub Copilot, Claude Code, Gemini CLI, and Google Antigravity.
- Installation by scope (`project` / `user`) and by individual skill name.
- `skills/README.md` with consolidated catalog, recommended workflow, and installation guide.

### Changed

- Root `README.md` expanded with skill catalog, conceptual model, integrated workflow, and installation instructions.

## [1.0.1] - 2026-10-22

### Added

- **`architecture-decision-advisor`** — Skill for architectural decisions, trade-offs, and ADRs (synchronous/asynchronous, Apigee, messaging).
- **`code-solution-designer`** — Skill for designing algorithms, types, and code structure before implementation in C#/.NET.

## [1.0.0] - 2026-10-19

### Added

- **`MVFC.AgentSkills`** — Core skill for functional specification and decomposition of .NET use cases, with templates and reference documentation.
- **`banking-test-engineer`** — Automated test engineering skill using FluentAssertions, NSubstitute, Bogus, and AutoFaker.
- **`pragmatic-technical-debt-review`** — Pragmatic technical debt review skill covering race conditions, idempotency, concurrency, and resilience.
- **`requirements-insight-analyst`** — Requirements refinement skill from Jira/Azure Boards cards, screenshots, and OpenAPI contracts.
- **`business-flow-documentation`** — Business flow documentation skill for post-implementation functional docs with Mermaid sequence diagrams.
- **`banking-innovation-lab`** — Banking ideation and MVP structuring skill with or without AI under technical and regulatory constraints.

[Unreleased]: https://github.com/Marcus-V-Freitas/MVFC.AgentSkills/compare/v2.1.0...HEAD
[2.1.0]: https://github.com/Marcus-V-Freitas/MVFC.AgentSkills/compare/v2.0.0...v2.1.0
[2.0.0]: https://github.com/Marcus-V-Freitas/MVFC.AgentSkills/compare/v1.1.0...v2.0.0
[1.1.0]: https://github.com/Marcus-V-Freitas/MVFC.AgentSkills/compare/v1.0.1...v1.1.0
[1.0.1]: https://github.com/Marcus-V-Freitas/MVFC.AgentSkills/compare/v1.0.0...v1.0.1
[1.0.0]: https://github.com/Marcus-V-Freitas/MVFC.AgentSkills/releases/tag/v1.0.0
