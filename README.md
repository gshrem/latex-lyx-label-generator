# LaTeX & LyX Label Generator

**Original creator: [Gilad Shrem](https://github.com/gshrem)**

A free, open-source, instruction-only plugin for generating concise, meaningful English labels for cross-references in **LaTeX** and **LyX** documents. It works with content in any language and across academic disciplines.

> **Installation note:** This repository provides an installable plugin source for **supported Codex / ChatGPT desktop local-marketplace workflows**. It is **not currently listed in the universal ChatGPT Plugins Directory**, and a GitHub installation does **not** provide `@` invocation in all ChatGPT web or mobile conversations.

## What it does

| Input | Example label |
| --- | --- |
| A section about compact metric spaces | `sec:compact-metric-spaces` |
| The fundamental theorem of calculus | `thm:fundamental-theorem-of-calculus` |
| A definition of positive semidefinite matrices | `def:positive-semidefinite-matrix` |
| A figure showing a protein interaction network | `fig:protein-interaction-network` |
| A binary-search algorithm | `alg:binary-search` |

- Supports sections, chapters, appendices, theorems, lemmas, definitions, equations, figures, tables, code listings, algorithms, and custom referenceable structures.
- Uses a relevant element-type prefix and **no more than five descriptive words** separated by hyphens.
- Accepts text, mathematical expressions, and LaTeX source written in **any language**; generates labels in English.
- Infers the semantic type of custom environments rather than blindly using technical environment names.
- Respects users' established naming conventions.
- Avoids duplicate labels in a batch or among supplied existing labels. **Document-wide uniqueness requires the complete set of existing labels.**
- By default, returns only the label key, ready for a LyX label field or for `\label{...}` in LaTeX.

## Use in a personal ChatGPT Project (recommended for ChatGPT web users)

This is a convenient way to use the generator repeatedly in private ChatGPT conversations **without installing a plugin**:

1. In ChatGPT, create a **new personal Project** (not a shared Project).
2. Open the Project's **instructions** from its settings or menu.
3. Copy the full contents of [`SKILL.md`](plugins/latex-lyx-label-generator/skills/latex-lyx-labels/SKILL.md) into the Project instructions, if the instructions field permits the full text. Alternatively, add `SKILL.md` as a Project file/source and set the Project instructions to: "Use the attached SKILL.md as the authoritative instructions for generating LaTeX and LyX labels. Follow its naming and output rules whenever I request a label."
4. Start a chat **inside that Project**, paste a theorem, definition, section heading, equation, or other element, and request a label.

The instructions or attached file remain available to subsequent chats **within that Project**. They do not automatically apply to chats outside it. Each person should create their **own private Project**: do not share a Project with strangers, because shared Projects may expose their chats and files to other members.

Project features and instruction/file limits depend on the user's ChatGPT account. If the full Skill cannot be pasted into Project instructions, use the Project-file alternative above. This is an independent setup for each user, **not a one-click install or an officially listed public plugin**.

## Install through the Git-backed plugin marketplace

**Compatible clients only.** OpenAI documents Git-backed plugin marketplaces for Codex, and local plugin installation through supported ChatGPT desktop workflows. This is separate from the public ChatGPT Plugins Directory.

1. In a supported Codex CLI installation, add this repository as a plugin marketplace:

   ```bash
   codex plugin marketplace add gshrem/latex-lyx-label-generator
   ```

2. Check the registered marketplace:

   ```bash
   codex plugin marketplace list
   ```

3. In the supported ChatGPT desktop plugin interface, restart the app if necessary, open the **Plugins Directory**, choose **Gilad Shrem's LaTeX Tools**, and install **LaTeX & LyX Label Generator**.

4. Use the plugin or its `latex-lyx-labels` skill in supported conversations. Start with a theorem, definition, section heading, or equation, and request a label.

Installation interfaces and availability depend on your client, account, and configuration. These instructions **do not** imply that installation from GitHub works across all regular ChatGPT web, Android, or iOS conversations.

### Manual installation and inspection

The packaged plugin is in [`plugins/latex-lyx-label-generator/`](plugins/latex-lyx-label-generator/), including the portable `plugin.json`, its `skills/` directory, metadata and icon. The repository's [`.agents/plugins/marketplace.json`](.agents/plugins/marketplace.json) advertises that directory as a local marketplace entry.

If your AI client supports standalone skills but not plugin marketplaces, use [`SKILL.md`](plugins/latex-lyx-label-generator/skills/latex-lyx-labels/SKILL.md) following that client's own skill-import instructions. Do not assume every client supports direct skill import.

## Attribution and licensing

**Original creator: Gilad Shrem**  
**Official source:** https://github.com/gshrem/latex-lyx-label-generator  
**Plugin source version:** `1.0.1`

This project is freely shareable and modifiable, provided the appropriate original attribution and applicable license notices are retained.

- **[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/):** Skill instructions, original prose/documentation and artwork. When redistributing adapted content, provide attribution and indicate changes.
- **[MIT](LICENSE-MIT.txt):** Machine-readable configuration and metadata files.
- See [full license scope](LICENSE.md), [attribution guidance](ATTRIBUTION.md), and [citation details](CITATION.cff).

You **do not** need to place attribution inside every label generated by the skill. Credit is relevant when distributing or adapting the project itself.

GitHub's **Cite this repository** feature uses `CITATION.cff` to display citation formats. GitHub forks and commit history also provide provenance, though neither prevents someone from removing credit from a separate copy.

## Privacy and support

The plugin operates solely through instructions within the host AI application and has **no publisher-operated server, telemetry, external API, or storage of users' conversations**. The host platform may process messages under its own privacy policy.

- [Support and bug reports](SUPPORT.md) via [GitHub Issues](https://github.com/gshrem/latex-lyx-label-generator/issues)
- [Privacy policy](PRIVACY.md)
- [Terms of use](TERMS.md)

This is an independent project, not affiliated with or endorsed by OpenAI, LaTeX Project, or LyX.
