# Templates

Starting points for new documents produced by the WG and its SIGs. Each template carries the correct `Document type`, all the required frontmatter fields (per [`document-metadata.md`](../document-metadata.md)), and the structural sections required by the [working mode](../working-mode.md).

| Template | For | File-naming pattern |
| --- | --- | --- |
| [`submission.md`](submission.md) | A submission to an external stakeholder — comments, contributions, feedback, or response to a call/consultation. | `deliverable-X-Y.md` (X.Y from the deliverables plan), in `[sig]/coordination/[stakeholder]/` or a dated subfolder. |
| [`white-paper.md`](white-paper.md) | A standalone analytical white paper. | Descriptive filename in `[sig]/whitepapers/`. |
| [`meeting-notes.md`](meeting-notes.md) | A meeting agenda → minutes document for a SIG plenary, task force, or governance committee. | `YYYY-MM-DD-mom-[group].md`, in the relevant `minutes/` folder. |

When using a template:

- Replace each `<placeholder>` in the YAML frontmatter with a concrete value, or leave the field empty when it doesn't apply (per the schema rules in `document-metadata.md`).
- Replace each `[placeholder]` in the body with concrete content (names, titles, dates, headings, etc.).
- Replace each `> [!TIP]` callout with the content it describes — the callout is an author instruction, not text to keep.
- Replace each `_TBD: ..._` block with the relevant boilerplate text once finalized.
