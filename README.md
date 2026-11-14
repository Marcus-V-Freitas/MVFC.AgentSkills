# .NET Functional Use Case Spec & Developer Skills Catalog

> 🇧🇷 [Versão em Português](README.pt-BR.md)

A catalog of **Agent Skills** specialized for C#/.NET software engineering, system architecture, requirements analysis, debugging, security, and the banking/corporate domain.

Designed for AI agents such as **GitHub Copilot**, **Claude Code**, **Gemini Code Assist / CLI**, and **Google Antigravity**.

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)
[![Skills](https://img.shields.io/badge/skills-20-brightgreen)](#skill-catalog)
[![Platforms](https://img.shields.io/badge/platforms-Copilot%20%7C%20Claude%20%7C%20Gemini%20%7C%20Antigravity-blueviolet)](#quick-install)

Designed for AI agents such as **GitHub Copilot**, **Claude Code**, **Gemini Code Assist / CLI**, and **Google Antigravity**.

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)
[![Skills](https://img.shields.io/badge/skills-20-brightgreen)](#skill-catalog)
[![Platforms](https://img.shields.io/badge/platforms-Copilot%20%7C%20Claude%20%7C%20Gemini%20%7C%20Antigravity-blueviolet)](#quick-install)

---

## Philosophy

The focus is not an isolated `Handler` class. The focus is the **complete business functionality**.

A business functionality may be implemented as:

```text
Handler / UseCase / CommandHandler / QueryHandler
ApplicationService / Service / Consumer
Processor / Job / Workflow
```

or a composition of these elements.

### Conceptual Model

```text
Business Functionality
        ↓
Entry Point
        ↓
Input Payload
        ↓
Validation
        ↓
Use-case Orchestrator
    ┌──────┼──────────┐
    ↓      ↓          ↓
 Service  Policy   Repository
    ↓                 ↓
External API        Database
    ↓
Messaging
        ↓
Possible Outputs
```

---

## Skill Catalog

### Specification & Design

| Skill                                                                              | Focus                                         | When to Use                                                                                                                  |
| :--------------------------------------------------------------------------------- | :-------------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------- |
| **[`dotnet-functional-use-case-spec`](./skills/dotnet-functional-use-case-spec/)** | Functional specification and decomposition    | Full mapping of input, validation, orchestration, outputs, errors, and use-case decomposition.                               |
| **[`architecture-decision-advisor`](./skills/architecture-decision-advisor/)**     | Architectural decisions, trade-offs, and ADRs | Choosing between sync/async communication, consistency, topology, Apigee, and messaging.                                     |
| **[`code-solution-designer`](./skills/code-solution-designer/)**                   | Algorithm design and internal code structure  | Designing classes, flow, and fit within the application before writing the C#/.NET implementation.                           |
| **[`implementation-plan-reviewer`](./skills/implementation-plan-reviewer/)**       | Implementation plan review                    | Validates feasibility, missing prerequisites, ordering, risks, and rollback of a technical plan before execution.            |
| **[`migration-strategy-planner`](./skills/migration-strategy-planner/)**           | Safe migration planning                       | Transitions between frameworks, schemas, libraries, services, or deployment topologies with controlled rollout and rollback. |

### Requirements & Analysis

| Skill                                                                        | Focus                                 | When to Use                                                                                                            |
| :--------------------------------------------------------------------------- | :------------------------------------ | :--------------------------------------------------------------------------------------------------------------------- |
| **[`requirements-insight-analyst`](./skills/requirements-insight-analyst/)** | Requirements refinement and analysis  | Translating Jira/Azure Boards cards, screenshots, and OpenAPI contracts into sequential flows and acceptance criteria. |
| **[`change-impact-analyzer`](./skills/change-impact-analyzer/)**             | Change impact mapping                 | Traces direct and transitive effects of a change across contracts, callers, data, tests, and operations.               |
| **[`codebase-explorer`](./skills/codebase-explorer/)**                       | Repository navigation and orientation | Explains entrypoints, modules, dependencies, state flow, and where to make a change. Ideal for onboarding.             |

### Quality & Testing

| Skill                                                                        | Focus                                    | When to Use                                                                                                          |
| :--------------------------------------------------------------------------- | :--------------------------------------- | :------------------------------------------------------------------------------------------------------------------- |
| **[`banking-test-engineer`](./skills/banking-test-engineer/)**               | Automated test engineering for C#/.NET   | Building complete unit/integration test suites with FluentAssertions, NSubstitute, Bogus, and AutoFaker.             |
| **[`test-quality-auditor`](./skills/test-quality-auditor/)**                 | Test suite quality audit                 | Assesses evidentiary strength, oracle quality, isolation, determinism, and missing risk coverage in existing suites. |
| **[`code-review-specialist`](./skills/code-review-specialist/)**             | PR and diff code review                  | Rigorous review of correctness, reliability, security, and regressions in code changes.                              |
| **[`behavior-preserving-refactor`](./skills/behavior-preserving-refactor/)** | Safe refactoring without behavior change | Simplification, decomposition, and duplication removal while preserving contracts and observable behavior.           |

### Debugging & Operations

| Skill                                                                              | Focus                                | When to Use                                                                                                    |
| :--------------------------------------------------------------------------------- | :----------------------------------- | :------------------------------------------------------------------------------------------------------------- |
| **[`evidence-driven-debugger`](./skills/evidence-driven-debugger/)**               | Evidence-based debugging             | Diagnosing crashes, wrong outputs, intermittent bugs, and unexplained failures with falsifiable hypotheses.    |
| **[`root-cause-investigator`](./skills/root-cause-investigator/)**                 | Incident analysis and postmortems    | Building a causal timeline, contributing factors, and prevention actions for incidents and recurring failures. |
| **[`performance-investigator`](./skills/performance-investigator/)**               | Performance regression investigation | Locates the dominant bottleneck in latency, throughput, CPU, memory, or I/O with controlled experiments.       |
| **[`observability-advisor`](./skills/observability-advisor/)**                     | Operational observability design     | Logs, metrics, traces, health signals, and diagnostic context to ensure visibility in production.              |
| **[`security-reviewer`](./skills/security-reviewer/)**                             | Defensive security review            | Identifies actionable risks in code, configuration, and flows: injection, data exposure, trust boundaries.     |
| **[`pragmatic-technical-debt-review`](./skills/pragmatic-technical-debt-review/)** | Pragmatic defect and risk review     | Concurrency, idempotency, race conditions, transactions, and message loss analysis.                            |

### Banking Domain

| Skill                                                                      | Focus                             | When to Use                                                                                       |
| :------------------------------------------------------------------------- | :-------------------------------- | :------------------------------------------------------------------------------------------------ |
| **[`banking-innovation-lab`](./skills/banking-innovation-lab/)**           | Banking ideation and pilot design | Structuring MVPs and opportunities with or without AI under technical and regulatory constraints. |
| **[`business-flow-documentation`](./skills/business-flow-documentation/)** | Business flow documentation (.md) | Post-implementation functional documentation in Markdown with Mermaid sequence diagrams.          |

---

## Integrated Workflow

Skills work synergistically throughout the engineering lifecycle:

```text
[Requirements / Card]
        ↓
  requirements-insight-analyst   (refine card, map branches and open questions)
        ↓
  architecture-decision-advisor  (if a system / messaging / ADR decision is needed)
        ↓
  implementation-plan-reviewer   (validate the plan before starting)
        ↓
  code-solution-designer         (if the solution requires a prior algorithm or design)
        ↓
  dotnet-functional-use-case-spec (full use-case specification and orchestrator)
        ↓
  banking-test-engineer          (generate the end-to-end test suite)
        ↓
  test-quality-auditor           (audit quality and coverage of the generated suite)
        ↓
  code-review-specialist         (review the diff before merge)
        ↓
  change-impact-analyzer         (impact analysis on contracts and consumers)
        ↓
  pragmatic-technical-debt-review (concurrency and resilience risk review)
        ↓
  observability-advisor          (design logs, metrics, and traces for production)
        ↓
  business-flow-documentation    (final business flow documentation)
```

**Support skills available at any stage:**

```text
  codebase-explorer            → unfamiliar repository orientation
  evidence-driven-debugger     → bug and failure diagnosis
  performance-investigator     → performance regression investigation
  root-cause-investigator      → postmortems and incident analysis
  security-reviewer            → defensive security review
  behavior-preserving-refactor → safe refactoring
  migration-strategy-planner   → migration planning
```

---

## Repository Structure

```text
.
├── skills/
│   ├── architecture-decision-advisor/
│   ├── banking-innovation-lab/
│   ├── banking-test-engineer/
│   ├── behavior-preserving-refactor/
│   ├── business-flow-documentation/
│   ├── change-impact-analyzer/
│   ├── code-review-specialist/
│   ├── code-solution-designer/
│   ├── codebase-explorer/
│   ├── dotnet-functional-use-case-spec/
│   ├── evidence-driven-debugger/
│   ├── implementation-plan-reviewer/
│   ├── migration-strategy-planner/
│   ├── observability-advisor/
│   ├── performance-investigator/
│   ├── pragmatic-technical-debt-review/
│   ├── requirements-insight-analyst/
│   ├── root-cause-investigator/
│   ├── security-reviewer/
│   ├── test-quality-auditor/
│   ├── install.ps1
│   ├── install.sh
│   └── README.md
├── CHANGELOG.md
├── CONTRIBUTING.md
├── LICENSE
├── README.md
└── README.pt-BR.md
```

---

## Quick Install

The installers configure skills in the directories recognized by each tool (`.github/skills`, `.claude/skills`, `.gemini/skills`, `.agents/skills`, or their user-profile equivalents):

### PowerShell (`install.ps1`)

```powershell
# Install all skills in the current project for all tools
pwsh ./skills/install.ps1

# Install in global user scope
pwsh ./skills/install.ps1 -Scope user

# Install a specific skill only
pwsh ./skills/install.ps1 -Skill dotnet-functional-use-case-spec
```

### Bash (`install.sh`)

```bash
# Install all skills in the current project
./skills/install.sh

# Install in user scope
./skills/install.sh all user

# Install a specific skill only
./skills/install.sh all project . dotnet-functional-use-case-spec
```

For detailed compatibility instructions and advanced parameters, see the [Skills Guide](skills/README.md).

---

## Contributing

Contributions are welcome! Please read the [Contributing Guide](CONTRIBUTING.md) before opening a pull request.

## License

This project is licensed under the [Apache License 2.0](LICENSE).

---

## Contributing

Contributions are welcome! Please read the [Contributing Guide](CONTRIBUTING.md) before opening a pull request.

## License

This project is licensed under the [Apache License 2.0](LICENSE).
