# Contributing

This repository holds the design documentation for the Local Agentic AI Platform. There is no implementation code yet, so contributions are feedback on the design and fixes to the documentation.

## Giving feedback

Open an issue with one of the [issue forms](https://github.com/SatyamChouksey-88/local-agentic-ai-platform/issues/new/choose):

- **Design feedback**: a concern, gap or suggestion about the design in the Project Book.
- **Question**: something in the book is unclear.
- **Typo or clarity**: a small wording or formatting fix.

Please name the chapter or section you are referring to.

## Proposing a change

The repository uses GitHub flow: `main` is the only long-lived branch, and every change arrives through a pull request.

```bash
git clone https://github.com/SatyamChouksey-88/local-agentic-ai-platform.git
cd local-agentic-ai-platform
git checkout -b docs/short-topic
# edit files
git commit -m "Clarify the evidence status table"
git push -u origin docs/short-topic
```

Then open a pull request into `main` and fill in the template.

## Writing rules

- Describe the platform as *designed* or *proposed*. Nothing in this repository runs yet.
- Every claim must come from Project Book v2.0. Keep the book's labels (Verified, Estimate, Unverified).
- Use phases and gates, not calendar dates.
- Save text files as UTF-8 without a BOM. `.editorconfig` and `.gitattributes` enforce this in most editors.
- Mermaid diagrams: use `flowchart`, `sequenceDiagram` or `stateDiagram-v2` only, with no `%%{init}%%` themes, fill colours, `click` or HTML in labels, so they stay readable in light and dark mode.

## New book versions

The PDF and DOCX for each version are attached to a [GitHub Release](https://github.com/SatyamChouksey-88/local-agentic-ai-platform/releases). Record each version in [CHANGELOG.md](CHANGELOG.md).

## Publishing

Merging into `main` deploys the `docs/` folder to [GitHub Pages](https://satyamchouksey-88.github.io/local-agentic-ai-platform/) through `.github/workflows/pages.yml`.
