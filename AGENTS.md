# Instructions for AI agents working in this repository

This repository is design documentation for the Local Agentic AI Platform. There is no implementation code.

- **Source of truth:** Project Book v2.0 in `docs/`. Do not use v1.0 material (the 13-agent catalogue, QA-first scope).
- **No invented content:** every claim, component, agent, number and phase must come from the book. Keep its labels (Verified, Estimate, Unverified).
- **Honest tense:** describe the platform as designed or proposed, never as if it runs. No CI, coverage, version or download badges.
- **Safety wording:** humans approve irreversible actions, merges are always by a person, secrets and payments are always denied, and the agents are supervised assistants, not autonomous.
- **Roadmap:** phases and Go/Hold/Stop gates, never calendar dates or Gantt charts.
- **Mermaid:** `flowchart`, `sequenceDiagram` or `stateDiagram-v2` only; no `%%{init}%%`, fill colours, `click`, icon packs, `@{ shape }` or HTML in labels; at most about 12 nodes.
- **Encoding:** write text files as UTF-8 without a BOM and with LF line endings. In Windows PowerShell 5.1, do not use `>`, `Out-File` or `Set-Content -Encoding utf8` to write files.
- **Ask the owner first** before pushing, deleting files or branches, rewriting history, changing repository visibility or settings, or choosing a licence.
- **Privacy:** do not mention an employer or client, or personal details beyond the author's name and GitHub profile.
