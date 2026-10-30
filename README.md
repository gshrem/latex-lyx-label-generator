# LaTeX & LyX Label Generator

A free, instruction-only ChatGPT plugin by **Gilad Shrem** that creates short, clear, semantically meaningful English labels for cross-references in LaTeX and LyX documents.

## What it does

Given a theorem, definition, section, equation, figure, table, algorithm, or another referenceable element, the plugin suggests a descriptive label such as:

- `sec:compact-metric-spaces`
- `thm:fundamental-theorem-of-calculus`
- `def:positive-semidefinite-matrix`
- `fig:protein-interaction-network`

Labels use semantic prefixes and at most five descriptive English words. The plugin accepts input in any language, respects user-defined naming conventions, and can avoid collisions with existing labels supplied by the user. Without the full set of existing labels, document-wide uniqueness cannot be guaranteed.

## Availability

The ChatGPT plugin is being prepared for public review. **It is not yet publicly installable.** This repository hosts the project's information and policies; it is not itself a hosted app or a ChatGPT installation link.

No separate server, API, user account, or payment is required to operate the skill. Its instructions run within a compatible host application such as ChatGPT.

## Publisher and policies

**Publisher:** Gilad Shrem (independent developer)

- [Support and bug reports](SUPPORT.md)
- [Privacy policy](PRIVACY.md)
- [Terms of use](TERMS.md)

This is an independent project and is not affiliated with or endorsed by OpenAI, LaTeX Project, or LyX.
