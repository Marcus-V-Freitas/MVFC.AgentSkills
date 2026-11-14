# Security Policy

## Supported Versions

The table below lists which versions of **MVFC.AgentSkills** currently receive security updates.

| Version | Supported          |
| ------- | ------------------ |
| 2.x     | ✅ Yes             |
| 1.1.x   | ✅ Yes             |
| 1.0.x   | ❌ No              |
| < 1.0   | ❌ No              |

---

## Reporting a Vulnerability

If you discover a security vulnerability in this repository, **please do not open a public GitHub issue.**

Instead, report it privately via one of the channels below:

- **GitHub Private Vulnerability Reporting** *(preferred)*:
  Navigate to the **Security** tab of this repository and click **"Report a vulnerability"**.
- **Email**: Contact the maintainer directly at the address listed in the GitHub profile.

Please include the following information in your report:

1. A clear description of the vulnerability.
2. Steps to reproduce or a proof-of-concept (PoC).
3. The affected version(s).
4. The potential impact (confidentiality, integrity, availability).

---

## Response Timeline

| Step | Target Time |
|------|------------|
| Acknowledgement of the report | ≤ 48 hours |
| Initial triage and severity assessment | ≤ 5 business days |
| Patch release (critical/high) | ≤ 15 business days |
| Public disclosure (after fix) | Coordinated with reporter |

---

## Scope

This project is a **collection of AI agent skills** (instruction files). The main security considerations are:

- **Prompt injection** — skill instructions that could cause an AI agent to execute unintended actions.
- **Sensitive data exposure** — skill templates that might inadvertently encourage storing or logging sensitive information.
- **Supply-chain concerns** — malicious content introduced through external contributions.

---

## Out of Scope

- Vulnerabilities in the AI models or platforms consuming these skills (e.g., GitHub Copilot, Claude, Gemini CLI, Antigravity). Report those to the respective vendors.
- General bugs or feature requests — use the [issue tracker](https://github.com/Marcus-V-Freitas/MVFC.AgentSkills/issues) instead.

---

## Repository Rename Notice

> This repository was previously named **`dotnet-functional-use-case-spec`**.
> It was renamed to **`MVFC.AgentSkills`** to better reflect its expanded scope
> as a general-purpose AI agent skill library.
> GitHub automatically redirects traffic from the old name.

---

## Attribution

We follow the [GitHub Coordinated Disclosure](https://docs.github.com/en/code-security/security-advisories/guidance-on-reporting-and-writing/about-coordinated-disclosure-of-security-vulnerabilities) model.
Security reporters who responsibly disclose vulnerabilities will be credited in the release notes unless they prefer to remain anonymous.
