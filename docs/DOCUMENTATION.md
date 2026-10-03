# Project Book v2.0: reading guide

**Local Agentic AI Platform: The Project Book, version 2.0 (3 October 2026).** Design stage: documentation only, no implementation code.

Use this guide to find the chapters you need without reading all 58 chapters and 7 appendices.

## Files

| File | Use it for |
|---|---|
| [Local-Agentic-AI-Platform-Project-Book-v2.0.pdf](Local-Agentic-AI-Platform-Project-Book-v2.0.pdf) | Reading, with all figures and clickable contents |
| [Local-Agentic-AI-Platform-Project-Book-v2.0.docx](Local-Agentic-AI-Platform-Project-Book-v2.0.docx) | Editable source for review comments |

Both files are also attached to the [v2.0.0 release](https://github.com/SatyamChouksey-88/local-agentic-ai-platform/releases/tag/v2.0.0). The [README](../README.md) gives a short overview with diagrams.

## Reading paths

| Reader | Read these parts | Time |
|---|---|---|
| Leadership | Chapter 1, then Chapters 48 to 50, 54 and 58 | 15 to 20 minutes |
| Team leads | Part B, plus your Team Pack in Chapters 9 and 33 | 30 minutes |
| Architects and engineers | Parts C, D and E | 2 hours |
| Infrastructure and finance | Part F and Chapter 50 | 30 minutes |
| Security and compliance | Section 18.7 and Chapters 21, 25 to 28, 30 and 55 | 30 minutes |

## Contents

### Part A: The big picture

1. Executive summary
2. How this project came about
3. The problem and the opportunity
4. Vision, positioning and scope
5. Why this platform: market, alternatives and build-vs-buy
6. Feasibility verdict: what is realistic and what is not

### Part B: How the product works

7. The product in plain language
8. The organisation model: people, agents and seats
9. Team Packs: how every team joins
10. End-to-end flow across teams
11. Personas: a working day before and after
12. How people interact with it
13. Walkthroughs: from request to result

### Part C: Technical design

14. Architecture overview
15. Task lifecycle: the state machine
16. The agent loop, and when to use more than one agent
17. The Prompt Architect agent
18. The Project Onboarding agent
19. Contracts between agents
20. Evidence and verification
21. Policy engine and approvals
22. Escalation
23. Context engine and memory
24. Model routing and cost control
25. Tools, MCP and connectors
26. The sandbox
27. Security
28. Data model
29. Observability and audit
30. Many teams, projects and users: multi-tenancy

### Part D: The agents

31. How agents are specified
32. The agent catalogue at a glance
33. Agent specifications and system prompts

### Part E: Building, integrating and running it

34. Build, buy and reuse
35. Technology stack
36. Repository structure and build order
37. Integration guide: connecting any project
38. Building the platform with AI coding assistants
39. Quality and testing strategy
40. CI/CD and releases of the platform
41. Operations: running the platform
42. Definition of Done

### Part F: Infrastructure, models and cost

43. Workload and the local-versus-cloud decision
44. Models: shortlist, licences and register
45. Hardware sizing
46. Deployment architecture and environments
47. Cost model

### Part G: Delivery, business case and governance

48. Phase-gate roadmap: start to end
49. Phase 1 pilot: KPIs and Go, Hold or Stop
50. Business case and ROI
51. Team, roles and responsibilities
52. The hero demo
53. Adoption and change management
54. Risks and mitigations
55. Compliance, privacy and licences
56. Future roadmap
57. Master checklist
58. Open decisions and next steps

### Appendices

- Appendix A. The 79 repositories: verdicts
- Appendix B. Verification of research claims
- Appendix C. What changed from version 1.0, and review triage
- Appendix D. Requirements traceability
- Appendix E. Mermaid sources for all diagrams
- Appendix F. Glossary
- Appendix G. References

All 22 figures in the book are also available as Mermaid source in Appendix E.

## Labels used in the book

| Label | Meaning |
|---|---|
| **Verified** | Checked against a primary source, or against two or more consistent reputable sources |
| **Estimate** | The author's own calculation, design target or interpretation; replace with measured numbers |
| **Unverified** | A single secondary source, or conflicting data; confirm before relying on it |
| **[R1]** | Research round 1 (2 October 2026): agent-runtime practice, security, evaluation, business case |
| **[R2]** | Research round 2 (3 October 2026): market, competitors, open-source licences, infrastructure, cost, compliance, build practice |
| **[R3]** | Research round 3 (3 October 2026): Prompt Architect, Project Onboarding, integration, company-wide use, stack, verification of earlier claims |
| **[New in 2.0]** | Design content added in this version, based on the owner's direction and four written reviews of version 1.0 |

Prices and benchmarks change quickly; re-check them before external use. The book is not legal advice.

## Version history

| Version | Date | What it contained |
|---|---|---|
| 0.1 | 2 October 2026 | First concept document and a Phase 1 code skeleton (not published here) |
| 1.0 | 2 October 2026 | Leadership briefing: runtime-first architecture, evidence gating and roadmap |
| 1.0 + Appendix C | 3 October 2026 | Version 1.0 extended with a catalogue of 13 agents (superseded) |
| **2.0** | **3 October 2026** | **This book**: company-wide scope (not QA-first), Prompt Architect and Project Onboarding, Team Packs, a 19-role catalogue and the full lifecycle |

See [CHANGELOG.md](../CHANGELOG.md) for the summary of each version.
