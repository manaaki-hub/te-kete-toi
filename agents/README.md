# Agent Architecture — Te Whare o ngā Kaitoi

Every file here is a Claude Code subagent definition (YAML frontmatter + system prompt). Install by copying into your project's `.claude/agents/`. All agents load `TIKANGA.md` first and obey it over any brief.

## Three layers

**1. Design specialists (`design/`)** — one agent per art form, deep in its own vocabulary, symmetry systems, materials, and documented meanings: kōwhaiwhai · tukutuku · whakairo · tokotoko · tā moko (knowledge/review only) · raranga-tāniko · toi-hou (contemporary/digital). Each also contributes a **design layer** to composite works so multiple specialists can co-produce one coherent piece.

**2. Culture layer (`culture/`)** — the significance layer sits between design and review: every motif choice must arrive with its documented meaning, source, tapu zone, and appropriateness argument.

**3. Review whānau (`review/`)** — kaumātua, kuia, whaea, matua, koro. Different lenses, same job: rigorous critique producing a **review pack for real human knowledge holders**. They never give final cultural approval — see `TIKANGA.md` §2.

## Composite works

For a piece needing several vocabularies (e.g. a digital artwork with kōwhaiwhai rhythm and tāniko borders), the pipeline runs specialists in parallel, then the toi-hou agent integrates layers under the significance layer's supervision, then the full review round runs on the composite. One coherent design, many accountable layers.

## Order of operations

`pipeline/workflow.md` is the contract. Skipping the culture layer or the human gate is a defect, not a shortcut.
