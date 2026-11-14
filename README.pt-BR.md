# MVFC.AgentSkills — Catálogo de Developer Skills

> 🇺🇸 [English version](README.md)

Catálogo de **Agent Skills** especializadas para engenharia de software C#/.NET, arquitetura de sistemas, análise de requisitos, debugging, segurança e ecossistema bancário/PJ.

Projetado para agentes de IA como **GitHub Copilot**, **Claude Code**, **Gemini Code Assist / CLI** e **Google Antigravity**.

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)
[![Skills](https://img.shields.io/badge/skills-20-brightgreen)](#catálogo-de-skills)
[![Plataformas](https://img.shields.io/badge/plataformas-Copilot%20%7C%20Claude%20%7C%20Gemini%20%7C%20Antigravity-blueviolet)](#instalação-rápida)

---

## Foco e Filosofia

O foco não é uma classe isolada chamada `Handler`. O foco é a **funcionalidade de negócio completa**.

Uma funcionalidade de negócio pode estar implementada como:

```text
Handler / UseCase / CommandHandler / QueryHandler
ApplicationService / Service / Consumer
Processor / Job / Workflow
```

ou uma composição desses elementos.

### Modelo Conceitual

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

## Catálogo de Skills

### Especificação & Design

| Skill                                                                              | Foco Principal                            | Quando Usar                                                                                                   |
| :--------------------------------------------------------------------------------- | :---------------------------------------- | :------------------------------------------------------------------------------------------------------------ |
| **[`dotnet-functional-use-case-spec`](./skills/dotnet-functional-use-case-spec/)** | Especificação e decomposição funcional    | Mapeamento completo de entrada, validação, orquestração, outputs, erros e decomposição de casos de uso.       |
| **[`architecture-decision-advisor`](./skills/architecture-decision-advisor/)**     | Decisões arquiteturais, trade-offs e ADRs | Escolha entre comunicação síncrona/assíncrona, consistência, topologia, Apigee e mensageria.                  |
| **[`code-solution-designer`](./skills/code-solution-designer/)**                   | Design de algoritmos e estrutura interna  | Desenho de algoritmos, tipos, fluxo e encaixe no código antes da implementação interna em C#/.NET.            |
| **[`implementation-plan-reviewer`](./skills/implementation-plan-reviewer/)**       | Revisão de planos de implementação        | Valida viabilidade, pré-requisitos, ordenação, riscos e rollback de um plano técnico antes da execução.       |
| **[`migration-strategy-planner`](./skills/migration-strategy-planner/)**           | Planejamento de migrações seguras         | Transições entre frameworks, schemas, bibliotecas, serviços ou topologias com rollout e rollback controlados. |

### Requisitos & Análise

| Skill                                                                        | Foco Principal                         | Quando Usar                                                                                                     |
| :--------------------------------------------------------------------------- | :------------------------------------- | :-------------------------------------------------------------------------------------------------------------- |
| **[`requirements-insight-analyst`](./skills/requirements-insight-analyst/)** | Análise e refinamento de requisitos    | Tradução de cards Jira/Azure Boards, prints e contratos em fluxos sequenciais acionáveis e critérios de aceite. |
| **[`change-impact-analyzer`](./skills/change-impact-analyzer/)**             | Mapeamento de impacto de mudanças      | Rastreia efeitos diretos e transitivos de uma mudança sobre contratos, callers, dados, testes e operações.      |
| **[`codebase-explorer`](./skills/codebase-explorer/)**                       | Navegação e orientação em repositórios | Explica entrypoints, módulos, dependências, fluxo de estado e onde realizar mudanças. Ideal para onboarding.    |

### Qualidade & Testes

| Skill                                                                        | Foco Principal                                  | Quando Usar                                                                                                       |
| :--------------------------------------------------------------------------- | :---------------------------------------------- | :---------------------------------------------------------------------------------------------------------------- |
| **[`banking-test-engineer`](./skills/banking-test-engineer/)**               | Engenharia de testes automatizados C#/.NET      | Criação de suítes completas de testes unitários/integração (FluentAssertions, NSubstitute, Bogus, AutoFaker).     |
| **[`test-quality-auditor`](./skills/test-quality-auditor/)**                 | Auditoria de qualidade de testes existentes     | Avalia força evidenteial, oráculos, isolamento, determinismo e cobertura de riscos ausentes em suítes existentes. |
| **[`code-review-specialist`](./skills/code-review-specialist/)**             | Code review de PRs e diffs                      | Revisão rigorosa de correctude, confiabilidade, segurança e regressões em mudanças de código.                     |
| **[`behavior-preserving-refactor`](./skills/behavior-preserving-refactor/)** | Refatoração segura sem mudança de comportamento | Simplificação, decomposição e remoção de duplicação preservando contratos e comportamento observável.             |

### Debugging & Operação

| Skill                                                                              | Foco Principal                            | Quando Usar                                                                                                       |
| :--------------------------------------------------------------------------------- | :---------------------------------------- | :---------------------------------------------------------------------------------------------------------------- |
| **[`evidence-driven-debugger`](./skills/evidence-driven-debugger/)**               | Debugging baseado em evidências           | Diagnóstico de crashes, outputs incorretos, bugs intermitentes e falhas inexplicadas com hipóteses falsificáveis. |
| **[`root-cause-investigator`](./skills/root-cause-investigator/)**                 | Análise de incidentes e postmortems       | Construção de timeline causal, fatores contribuintes e ações de prevenção para incidentes e falhas recorrentes.   |
| **[`performance-investigator`](./skills/performance-investigator/)**               | Investigação de regressões de performance | Localiza o bottleneck dominante em latência, throughput, CPU, memória ou I/O com experimentos controlados.        |
| **[`observability-advisor`](./skills/observability-advisor/)**                     | Design de observabilidade operacional     | Logs, métricas, traces, health signals e contexto diagnóstico para garantir visibilidade em produção.             |
| **[`security-reviewer`](./skills/security-reviewer/)**                             | Revisão de segurança defensiva            | Identifica riscos acionáveis em código, configuração e fluxos: injection, exposição de dados, trust boundaries.   |
| **[`pragmatic-technical-debt-review`](./skills/pragmatic-technical-debt-review/)** | Code review de defeitos e riscos reais    | Análise pragmática de concorrência, idempotência, race conditions, transações e perda de mensagens.               |

### Domínio Bancário

| Skill                                                                      | Foco Principal                          | Quando Usar                                                                                         |
| :------------------------------------------------------------------------- | :-------------------------------------- | :-------------------------------------------------------------------------------------------------- |
| **[`banking-innovation-lab`](./skills/banking-innovation-lab/)**           | Ideação bancária e desenho de pilotos   | Estruturação de MVPs e oportunidades com ou sem IA sob restrições técnicas e arquiteturais.         |
| **[`business-flow-documentation`](./skills/business-flow-documentation/)** | Documentação de fluxos de negócio (.md) | Criação de documentação funcional pós-implementação em Markdown com diagramas Mermaid de sequência. |

---

## Fluxo de Trabalho Integrado

As skills atuam sinergicamente durante o ciclo de engenharia:

```text
[Requisitos / Card]
        ↓
  requirements-insight-analyst   (refina card, mapeia bifurcações e dúvidas)
        ↓
  architecture-decision-advisor  (se houver decisão entre sistemas / mensageria / ADR)
        ↓
  implementation-plan-reviewer   (valida o plano antes de começar)
        ↓
  code-solution-designer         (se a solução interna exigir algoritmo ou desenho prévio)
        ↓
  dotnet-functional-use-case-spec (especificação completa do caso de uso e orquestrador)
        ↓
  banking-test-engineer          (geração da suíte de testes ponta a ponta)
        ↓
  test-quality-auditor           (auditoria de qualidade e cobertura da suíte gerada)
        ↓
  code-review-specialist         (revisão do diff antes do merge)
        ↓
  change-impact-analyzer         (análise de impacto sobre contratos e consumidores)
        ↓
  pragmatic-technical-debt-review (revisão de riscos de concorrência e resiliência)
        ↓
  observability-advisor          (design de logs, métricas e traces para produção)
        ↓
  business-flow-documentation    (documentação final do fluxo de negócio implementado)
```

**Skills de suporte disponíveis em qualquer etapa:**

```text
  codebase-explorer            → orientação em repositórios desconhecidos
  evidence-driven-debugger     → diagnóstico de bugs e falhas
  performance-investigator     → investigação de regressões de performance
  root-cause-investigator      → postmortems e análise de incidentes
  security-reviewer            → revisão de segurança defensiva
  behavior-preserving-refactor → refatoração segura
  migration-strategy-planner   → planejamento de migrações
```

---

## Estrutura do Repositório

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

## Instalação Rápida

Os instaladores configuram as skills nos diretórios reconhecidos por cada ferramenta (`.github/skills`, `.claude/skills`, `.gemini/skills`, `.agents/skills` ou seus equivalentes no perfil de usuário):

### PowerShell (`install.ps1`)

```powershell
# Instala todas as skills no projeto atual para todas as ferramentas
pwsh ./skills/install.ps1

# Instala no escopo global do usuário
pwsh ./skills/install.ps1 -Scope user

# Instala apenas uma skill específica (ex: dotnet-functional-use-case-spec)
pwsh ./skills/install.ps1 -Skill dotnet-functional-use-case-spec
```

### Bash (`install.sh`)

```bash
# Instala todas as skills no projeto atual
./skills/install.sh

# Instala no escopo de usuário
./skills/install.sh all user

# Instala apenas uma skill específica
./skills/install.sh all project . dotnet-functional-use-case-spec
```

Para instruções detalhadas de compatibilidade e parâmetros avançados, consulte o [Guia de Skills](skills/README.md).

---

## Contribuição

Contribuições são bem-vindas! Leia o [Guia de Contribuição](CONTRIBUTING.md) antes de abrir um pull request.

## Licença

Este projeto está licenciado sob a [Apache License 2.0](LICENSE).
