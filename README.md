# Local Agentic AI Platform

**An AI-assisted software engineering platform** — a supervised multi-agent runtime that runs on **company-controlled infrastructure**.

| | |
|---|---|
| **Author** | Satyam Chouksey |
| **Version** | 2.0 (3 October 2026) |
| **Status** | Draft for leadership review — concept & design documentation |

---

## Overview

The **Local Agentic AI Platform** is a reusable **Agent Runtime** where specialised AI agents support every delivery team (Development, QA, BA/Product, Scrum/PM, DevOps/SRE, Security, Documentation) **under human leadership**. Agents are supervised assistants, not autonomous employees.

### Why this exists

- AI adoption in software teams is widespread, but **trust in AI output remains low**.
- The goal is not more AI output — it is output that can be **trusted, measured, and governed**.

### Core principle: trust through evidence

Work is accepted only when **deterministic evidence** proves it (passing tests, exit codes, traces, diffs, cited sources) — never because a model claims it is done.

- Irreversible actions (merge, deploy, delete data) require **explicit human approval** via a policy engine.
- Agents never receive raw secrets.
- Repository, ticket, and web content is treated as **data**, not as instructions.

### What makes it different

- Runs on **infrastructure the company controls** (not SaaS-only).
- Combines **open-weight local models**, **evidence gating**, **human-approval policy**, and **multi-team configuration** (Team Packs).
- Integrates with existing tools (CI, test frameworks, IDEs) and exposes capabilities via **MCP** (Model Context Protocol) to Copilot, Claude Code, Cursor, and similar assistants.

---

## Documentation (Project Book)

The full vision, architecture, agent catalogue, build plan, infrastructure, delivery, and research live in **The Project Book**:

| Format | File |
|--------|------|
| **PDF** (recommended for reading) | [`docs/Local-Agentic-AI-Platform-Project-Book-v21.pdf`](docs/Local-Agentic-AI-Platform-Project-Book-v21.pdf) |
| **Word** (editable source) | [`docs/Local-Agentic-AI-Platform-Project-Book-v2.docx`](docs/Local-Agentic-AI-Platform-Project-Book-v2.docx) |

See [`docs/DOCUMENTATION.md`](docs/DOCUMENTATION.md) for a structured table of contents and reading guide.

---

## Architecture (high level)

```
Request -> Prompt Architect -> Planner -> Runtime Core -> Workers (tools via policy gateway) -> Verifier -> Result / Escalation
                ^                              ^
         Project Onboarding              Context, policy, model routing
```

| Component | Responsibility |
|-----------|----------------|
| **Interfaces** | Team chat, web console, IDE (MCP), CLI, CI hooks — single task API |
| **Prompt Architect** | Structures every request; ask, assume, or proceed; prompt library |
| **Project Onboarding** | Maps the project; safe reads; **Project Brief** for all agents |
| **Planner** | Verifiable steps; complexity check; approval markers |
| **State machine & task store** | LangGraph + Postgres checkpointer; retries, budgets, resume |
| **Context engine** | High-signal context within token budgets |
| **Policy engine** | Allow / deny / require approval per tool call |
| **Model router** | Step-level routing, privacy flags, fallbacks, budgets |
| **Verifier** | Evidence checks in code; accept, repair, or escalate |

---

## Agent catalogue (19 roles)

Roles are a **menu**, enabled per team via **Team Packs**. Phase 1 focuses on platform agents, Failure Analyst, Verifier, and a second-team demo (Requirements Analyst).

| Agent | Group | Phase |
|-------|-------|-------|
| Orchestrator | Platform | 3 |
| **Prompt Architect** | Platform | **1** |
| **Project Onboarding** | Platform | **1** |
| **Planner** | Platform | **1** |
| **Verifier** | Platform | **1** |
| **Failure Analyst** | Delivery core | **1** |
| Test Designer | QA | 2 |
| Automation Engineer | QA | 2 |
| QA Lead | QA | 2 |
| Dev Lead | Development | 2 |
| Architect | Development | 2 |
| Backend Developer | Development | 2 |
| Frontend Developer | Development | 2 |
| Code Reviewer | Development | 2 |
| Requirements Analyst | BA & Product | 3 (demo in 1) |
| Scrum Master assistant | Scrum & PM | 3 |
| DevOps & SRE Lead | DevOps & SRE | 3 |
| Security Analyst | Security | 3 |
| Technical Writer | Documentation | 4 |

Full specifications and system prompts are in **Part D** of the Project Book.

---

## Technology stack (recommended)

| Layer | Choice |
|-------|--------|
| Core runtime | Python 3.12+, LangGraph, Pydantic |
| API | FastAPI |
| UI / CLI / IDE | TypeScript (console, MCP server, CLI) |
| Task persistence | Postgres (LangGraph checkpointer) |
| Model gateway | LiteLLM + routing rules |
| Policy | YAML rules (OPA/Cedar optional) |

Alternatives and rationale are documented in Chapter 35 of the Project Book.

---

## Delivery model

- **Five phase gates (0–4)** plus continuous operation — exit criteria per gate, no fixed calendar promises.
- **Phase 1 pilot**: CI/build failure diagnosis (shared by Dev, QA, DevOps); platform proof via a second workflow (requirement to user stories) on the **same runtime** with configuration only.
- **Estimated effort (Phases 0–1)**: ~18–29 person-weeks over ~4 months including pilot (Estimate — see book).

---

## Who should read what

| Reader | Focus | Time |
|--------|--------|------|
| Leadership / board | Executive summary, roadmap, business case, risks | 15–20 min |
| Team leads | Product model, Team Packs, your pack chapter | ~30 min |
| Architects & engineers | Parts C, D, E (design, agents, build) | ~2 hours |
| Infrastructure & finance | Part F, cost model | ~30 min |
| Security & compliance | Policy, sandbox, data, compliance chapters | ~30 min |

---

## Labels in the book

| Label | Meaning |
|-------|---------|
| **Verified** | Primary source or multiple consistent reputable sources |
| **Estimate** | Internal calculation or design target — replace with measured data |
| **Unverified** | Single secondary source or conflicting data — confirm before use |

---

## Repository contents

```
.
├── README.md
├── docs/
│   ├── DOCUMENTATION.md
│   ├── Local-Agentic-AI-Platform-Project-Book-v21.pdf
│   └── Local-Agentic-AI-Platform-Project-Book-v2.docx
└── .gitignore
```

Implementation code (Phase 0/1 skeleton) is described in the Project Book; this repository currently publishes **version 2.0 design documentation** for review and alignment.

---

## Scope note

This is an **internal product concept**. It is not tied to any specific client or customer environment.

---

## License

Documentation copyright (c) Satyam Chouksey. Specify a license before open-sourcing implementation code.

---

## Contact

**Satyam Chouksey** — project author and owner of the v2.0 Project Book.
