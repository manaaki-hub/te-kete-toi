# Te Kete Toi

**A multi-agent Māori design intelligence system — grounded in documented mātauranga, governed by tikanga, with humans holding the final word.**

Te Kete Toi gives AI coding agents (Claude Code, Cursor, and compatible tools) a structured knowledge base of toi Māori — traditional and contemporary — plus a layered agent architecture: specialist design agents for each art form, a cultural significance layer, and a whānau of reviewer agents (kaumātua, kuia, whaea, matua, koro) who critique work and prepare it for **real human sign-off**.

> He atarangi te AI — AI is a shadow. It can carry knowledge, apply craft, and ask the right questions. It cannot hold mana or speak for tikanga. Every output of this system that touches cultural significance ends at a human gate.

## What's in the kete

| Layer | Path | What it does |
|---|---|---|
| **Knowledge** | `docs/` | Pattern glossary (kōwhaiwhai, tukutuku, whakairo, tāniko, tā moko), regional/iwi style notes, credited designer directory, annotated sources |
| **Design agents** | `agents/design/` | Specialists: kōwhaiwhai, tukutuku, whakairo, tokotoko, tā moko (knowledge/review only), raranga & tāniko, toi hou (contemporary/digital) |
| **Culture layer** | `agents/culture/` | Significance layer — checks meaning, context, and appropriateness of every design decision |
| **Review whānau** | `agents/review/` | Kaumātua, kuia, whaea, matua, koro reviewer agents + the review pack template for human sign-off |
| **Pipeline** | `pipeline/` | The full workflow: brief → specialist design → culture check → review rounds → human gate |
| **Design system** | `design-system/` | `DESIGN.md` + `theme.css` for use with styleseed, open-design, and claude-design-skill |
| **Assets** | `assets/patterns/` | Approved, licensed, or whānau-supplied pattern SVGs — with provenance rules |

## How the agents work together

```
Brief
  └─► Specialist design agent (e.g. tokotoko, kōwhaiwhai)
        └─► Significance layer (meaning, context, tapu/noa check)
              └─► Review whānau (kaumātua · kuia · whaea · matua · koro)
                    └─► Designer agents re-critique against review findings
                          └─► REVIEW PACK → real kaumātua / knowledge holders
                                └─► Human approval → final artwork
```

No stage may be skipped. See [`pipeline/workflow.md`](pipeline/workflow.md).

## Quick start

1. Clone this repo alongside your project.
2. Copy `agents/` into your project's `.claude/agents/` (each file is a Claude Code subagent definition).
3. Copy `design-system/theme.css` and `DESIGN.md` into your design tooling (works with [styleseed](https://github.com/manaaki-hub/styleseed), [open-design](https://github.com/manaaki-hub/open-design), [claude-design-skill](https://github.com/manaaki-hub/claude-design-skill)).
4. Read [`TIKANGA.md`](TIKANGA.md) before producing anything. It is not optional.
5. Put only **provenanced** pattern assets in `assets/patterns/` — see the rules there.

## Hard rules (summary — full version in TIKANGA.md)

- **No generation of moko for or about people.** The tā moko agent educates and reviews only.
- **No imitation of living artists' identifiable styles.** Designers are credited and linked, never cloned.
- **Iwi/hapū-specific designs require iwi/hapū authority.** Documented regional attribution is knowledge; using it is a permission question.
- **AI output is never the final cultural authority.** The review whānau prepares the questions; people answer them.
- **Provenance travels with every asset.** No pattern enters the system without a source, licence, and (where relevant) permission trail.

## Why this exists

AI design tools default to Stripe-and-Linear minimalism and, when asked for Māori design, produce culturally wrong approximations. Te Kete Toi replaces improvisation with documented knowledge, replaces flattening with specialist depth, and replaces "the model decided" with a review structure modelled on how toi Māori has always been governed — by the people who hold the knowledge.

## Status

Active development. The knowledge base is built from freely available, citable sources (see `docs/sources.md`). Corrections from knowledge holders are welcome and take precedence — open an issue.

## Licence

Code and structure: MIT. Mātauranga Māori referenced here remains the taonga of its iwi, hapū, and whānau — see `TIKANGA.md`. This repo asserts no ownership over any cultural knowledge it documents.
