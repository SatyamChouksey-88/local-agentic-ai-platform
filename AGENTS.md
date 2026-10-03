# Instructions for AI agents working in this repository

This repository is design documentation for the Local Agentic AI Platform. There is no implementation code.

- **Source of truth:** Project Book v2.0 in `docs/`. Do not use v1.0 material (the 13-agent catalogue, QA-first scope).
- **No invented content:** every claim, component, agent, number and phase must come from the book. Keep its labels (Verified, Estimate, Unverified) and name the chapter.
- **Honest tense:** describe the platform as designed or proposed, never as if it runs. The planned CLI is not published, so never add install or run commands for it.
- **Badges:** only status, book version, docs site and last commit. No CI, coverage, download-count or package badges.
- **Safety wording:** humans approve irreversible actions, merges are always by a person, secrets and payments are always denied, and the agents are supervised assistants, not autonomous.
- **Company-wide:** describe every delivery team; do not make QA or any single team the centre of the story.
- **Roadmap:** phases and Go/Hold/Stop gates, never calendar dates, durations or Gantt charts. Effort is stated in person-weeks and labelled Estimate.
- **Mermaid:** `flowchart`, `sequenceDiagram` or `stateDiagram-v2` only; `accTitle` and `accDescr` are welcome; no `%%{init}%%`, fill colours, `click`, icon packs, `@{ shape }` or HTML (such as `<br>`) in labels; at most about 12 nodes.
- **Consistency:** keep `README.md`, `docs/DOCUMENTATION.md` and `docs/index.html` consistent with each other (reading paths, labels, phases and file names).
- **Book files:** never edit the PDF or DOCX. A new book version comes from the author, with a CHANGELOG entry and a GitHub Release.
- **Encoding:** write text files as UTF-8 without a BOM and with LF line endings. In Windows PowerShell 5.1, do not use `>`, `Out-File` or `Set-Content -Encoding utf8` to write files.
- **Ask the owner first** before pushing, deleting files or branches, rewriting history, changing repository visibility or settings, or choosing a licence.
- **Privacy:** do not mention an employer or client, or personal details beyond the author's name and GitHub profile.
