# 🧓 UX Older People — Claude Agent Skill

> Evidence-based UX design rules for older adults (60+). Backed by 40+ peer-reviewed studies from 12+ countries.

[![Agent Skill](https://img.shields.io/badge/Agent_Skill-Claude_%7C_Codex-blue)](https://agentskills.io)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Studies](https://img.shields.io/badge/Research_Sources-40%2B_studies-orange)](/ux-older-people/references/research-sources.md)

---

## What is this?

A Claude skill that automatically applies age-friendly UX design rules whenever you're designing screens, components, or flows for older adults. Works with Claude.ai, Claude Code, and any tool that supports the [Agent Skills standard](https://agentskills.io).

**Example prompts that trigger the skill:**

- "Design an onboarding flow for a health app for seniors"
- "Review this checkout screen for age-friendliness"
- "Create a home page for an app targeting adultos mayores"
- "Make this form accessible for older adult users"

## What it covers

| Area | Key rules |
|---|---|
| **Touch Targets** | Min 16mm buttons, 3mm spacing, upper-right positioning |
| **Typography** | 18px body min, 7:1 contrast, sans-serif, adjustable size |
| **Color** | Light mode default, no red text, no blue-only elements |
| **Icons** | Always icon + text label, skeuomorphic > flat |
| **Navigation** | Linear paths, max 2 levels deep, always-visible nav |
| **Input/Forms** | Selection > typing, voice input, one field per screen |
| **Onboarding** | Step-by-step, no jargon, explain "why" at each step |
| **Errors** | Undo everywhere, confirm destructive actions, no dead ends |
| **Feedback** | Haptic + visual + audio, extended display times |
| **Privacy/Trust** | No dark patterns, no ads, human support access |
| **Devices** | Specific rules for mobile, tablet, and desktop |
| **Emotional** | Warm tone, no patronizing, support family involvement |

## Research basis

Every rule is grounded in peer-reviewed research from:

- **NNGroup** — 3 rounds of research, 123 participants, 5 countries, ~20 years
- **JMIR mHealth (2023)** — Systematic review, Spain/Australia/China collaboration
- **Springer (2025)** — 1,556 records reviewed, 132 articles, Iran
- **Monash University (2025)** — Focus groups + AdaptForge adaptive UI, Australia
- **PMC/NIH** — Multiple studies on haptics, icons, cognitive load
- **China MIIT** — Government regulations for age-friendly apps
- **European Accessibility Act** — EU law enforceable since June 2025
- Studies from **Korea, Japan, Saudi Arabia, Malaysia, Thailand, UK, Germany, US**

Full bibliography: [`ux-older-people/references/research-sources.md`](ux-older-people/references/research-sources.md)

---

## Installation

### Claude.ai (recommended)

1. Download the `.skill` file from [Releases](../../releases)
2. Open Claude.ai → Settings → Skills
3. Upload the `.skill` file
4. Done — the skill activates automatically when relevant

### Claude Code

```bash
# Personal (all projects)
cp -r ux-older-people/ ~/.claude/skills/

# Project-specific
cp -r ux-older-people/ .claude/skills/
```

### OpenAI Codex CLI

```bash
cp -r ux-older-people/ ~/.codex/skills/
```

### Manual

Copy the `ux-older-people/` folder into your agent's skills directory. The skill uses the standard [Agent Skills format](https://agentskills.io) — a `SKILL.md` with YAML frontmatter.

---

## File structure

```
ux-older-people/
├── SKILL.md                          # Main skill (267 lines, 12 sections)
└── references/
    └── research-sources.md           # Full bibliography (197 lines)
```

---

## Regulatory frameworks covered

- **WCAG 2.2** Level AA (minimum) / AAA (recommended)
- **European Accessibility Act (EAA)** — EU, since June 28, 2025
- **China MIIT Age-Friendly Regulations** — 2021+
- **ADA** — Americans with Disabilities Act
- **EN 301 549** — European ICT accessibility standard

---

## Contributing

Contributions welcome! If you have:

- **New research** — Open an issue with the study link and key findings
- **Rule improvements** — Open a PR with the change and the study backing it
- **Bug reports** — If a rule produces bad design output, let us know

Please keep all rules evidence-based. No opinions without citations.

---

## License

MIT — use it freely, commercially or otherwise.

---

## Credits

Created with research compiled from 40+ peer-reviewed studies. See the full [research sources](ux-older-people/references/research-sources.md) for attribution.
