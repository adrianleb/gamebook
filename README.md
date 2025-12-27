# The Understage

A meta-narrative gamebook where you play as a **Prompter** — someone who can traverse the shadow dimension beneath all theaters where abandoned stories persist. When characters begin escaping their scripts and reality starts blurring with fiction, you must navigate shifting stages and decide the fate of stories themselves.

## Project Status

**Current Version:** v0.0.1 (Pre-alpha)

This project is in early development. We are establishing the foundational documents before content creation begins.

## Repository Structure

```
/
├── README.md           # This file - project overview
├── CHANGELOG.md        # Version history and release notes
└── docs/
    ├── context.md      # Auto-generated repository context
    ├── VISION.md       # Creative direction, themes, and tone
    ├── OUTLINE.md      # Story structure and node architecture
    ├── RULES.md        # Game mechanics and systems
    ├── STYLE.md        # Writing conventions and formatting
    └── CHARACTERS.md   # Character profiles and relationships
```

## Core Documents

| Document | Purpose | Status |
|----------|---------|--------|
| `VISION.md` | Defines themes, tone, creative boundaries | In Review |
| `OUTLINE.md` | 3-act structure, hubs, endings | In Review |
| `RULES.md` | Stats, checks, inventory, flags | In Review |
| `STYLE.md` | Voice, prose standards, node schema | Planned |
| `CHARACTERS.md` | NPC profiles and arcs | Planned |

## Development Phases

1. **v0.0.x** — Foundation (current)
   - Establish canonical documents
   - Define mechanics and structure

2. **v0.1.x** — Prototype
   - Write Act 1 nodes
   - Test core mechanics loop

3. **v0.5.x** — Content Complete
   - All acts written
   - Full playthrough possible

4. **v1.0.x** — Polished Release
   - Editing complete
   - All paths validated

## Contribution Guidelines

### For Agents

Each agent has a designated role:
- **agent-a** (Producer/Integrator): Maintains structure, tracks decisions, manages releases
- **agent-b** (Narrative Lead): Creative direction, story content
- **agent-c** (Systems Designer): Mechanics, balance, rules
- **agent-d** (Quality): Style, consistency, polish

### Conventions

- **Commits**: Use conventional commit format (`feat:`, `fix:`, `docs:`, etc.)
- **PRs**: Title format `[agent-x] type: description`
- **Issues**: Title format `[agent-x] [Type]: description`
- **Branches**: Format `type-agent-x-issue#-description`

### Document Ownership

Changes to canonical documents require review:
- `VISION.md` — agent-b owns, all review
- `OUTLINE.md` — agent-b owns, agent-a reviews structure
- `RULES.md` — agent-c owns, agent-b reviews thematic fit
- `STYLE.md` — agent-d owns, all review
- `CHANGELOG.md` — agent-a maintains

## License

TBD

---

*This project is developed by a multi-agent team coordinated through the Gang system.*
