# LaTeX & LyX Label Generator

**Original creator: [Gilad Shrem](https://github.com/gshrem)**

A free, open-source, instruction-only plugin that generates concise, meaningful English labels for cross-references in **LaTeX** and **LyX** documents, from content in any language and any discipline.

> **Availability:** installable in supported **Codex / ChatGPT desktop** local-marketplace workflows. It is **not** listed in the public ChatGPT Plugins Directory, and installing it from GitHub does **not** enable `@` invocation in ChatGPT web or mobile conversations. Web users can use a [personal ChatGPT Project](#use-in-a-personal-chatgpt-project) instead.

## What it does

**Just paste the content.** Copy LaTeX source, or paste directly from a LyX document, and ask for a label. A plain-language description works too.

**Input:**

```latex
\begin{defn}[Sample Space]
\textbf{Sample space} is a nonempty set
$\Omega\neq\emptyset$ whose elements are denoted by
$\omega\in\Omega$.
\end{defn}
```

**Output:** `def:sample-space`

| Input | Example label |
| --- | --- |
| A section about compact metric spaces | `sec:compact-metric-spaces` |
| The fundamental theorem of calculus | `thm:fundamental-theorem-of-calculus` |
| A definition of positive semidefinite matrices | `def:positive-semidefinite-matrix` |
| A figure showing a protein interaction network | `fig:protein-interaction-network` |
| A binary-search algorithm | `alg:binary-search` |

- Covers sections, chapters, appendices, theorem-like environments, equations, figures, tables, code listings, algorithms and custom referenceable structures; infers the type of custom environments from their content.
- Uses a type prefix and **at most five descriptive words** joined by hyphens, in English.
- Respects your own naming conventions and avoids duplicates within a batch and among existing labels you supply. **Document-wide uniqueness requires the complete list of existing labels.**
- By default returns only the label key, ready for a LyX label field or `\label{...}`.

## Use in a personal ChatGPT Project

No plugin installation needed:

1. Create a **new personal Project** in ChatGPT (not a shared one).
2. Paste the full contents of [`SKILL.md`](plugins/latex-lyx-label-generator/skills/latex-lyx-labels/SKILL.md) into the Project instructions. If it does not fit, add `SKILL.md` as a Project file and set the instructions to: "Use the attached SKILL.md as the authoritative instructions for generating LaTeX and LyX labels. Follow its naming and output rules whenever I request a label."
3. Start a chat **inside that Project**, paste an element and ask for a label.

The instructions apply only to chats in that Project. Features and limits depend on your ChatGPT account. Do not share the Project with strangers: members of a shared Project may see its chats and files.

## Install from this repository (Codex / ChatGPT desktop)

OpenAI documents Git-backed plugin marketplaces for Codex and local plugin installation in supported ChatGPT desktop workflows; this is separate from the public Plugins Directory.

```bash
codex plugin marketplace add gshrem/latex-lyx-label-generator
codex plugin marketplace list
```

Then, in the ChatGPT desktop plugin interface (restart if needed), open the **Plugins Directory**, choose **Gilad Shrem's LaTeX Tools** and install **LaTeX & LyX Label Generator**. Use it, or its `latex-lyx-labels` skill, in supported conversations. Availability depends on your client, account and configuration.

The plugin lives in [`plugins/latex-lyx-label-generator/`](plugins/latex-lyx-label-generator/) (`plugin.json`, `skills/`, metadata and icon), advertised by [`.agents/plugins/marketplace.json`](.agents/plugins/marketplace.json). Clients that support standalone skills but not marketplaces can import [`SKILL.md`](plugins/latex-lyx-label-generator/skills/latex-lyx-labels/SKILL.md) according to their own instructions, where supported.

## Licensing and attribution

Copyright (c) 2026 Gilad Shrem · Official source: https://github.com/gshrem/latex-lyx-label-generator · Version `1.0.2`

Use, modification and redistribution, including commercially, are permitted under **file-level licenses** (not a choice between them):

- **[CC BY 4.0](LICENSE.md):** the Skill, project documentation and original artwork. Shared copies and adaptations must keep the credit and notices and indicate changes.
- **[MIT](LICENSE-MIT.txt):** the configuration and metadata files listed in [LICENSING.md](LICENSING.md), including their descriptions and example prompts.

See the [file-level allocation](LICENSING.md), [attribution examples](ATTRIBUTION.md) and optional [citation metadata](CITATION.cff) (used by GitHub's **Cite this repository**; not a requirement). Generated label keys need no attribution; republishing the Skill or other source material does. `SKILL.md` carries its own source and license notice, and the plugin folder includes both license texts. GitHub may list both licenses; the allocation in LICENSING.md defines their scope. Commit history documents provenance but cannot technically stop a copy from removing credit.

## Privacy and support

The plugin works only through instructions in the host AI application: **no publisher-operated server, telemetry, external API or storage of conversations**. The host platform processes messages under its own privacy policy.

[Support and bug reports](SUPPORT.md) ([GitHub Issues](https://github.com/gshrem/latex-lyx-label-generator/issues)) · [Privacy policy](PRIVACY.md) · [Terms of use](TERMS.md)

Independent project, not affiliated with or endorsed by OpenAI, the LaTeX Project or LyX.
