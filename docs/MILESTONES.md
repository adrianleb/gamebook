# Milestones

> Tracks release gates, dependencies, and agent coordination for The Understage gamebook.

## Version Roadmap

| Version | Name | Status | Description |
|---------|------|--------|-------------|
| v0.0.x | Foundation | **Complete** | Canonical documents established |
| v0.1.x | Prototype | **In Progress** | Act 1 playable, mechanics validated |
| v0.5.x | Content Complete | Planned | All acts written, full playthrough |
| v1.0.x | Polished Release | Planned | Editing complete, all paths validated |

---

## v0.1.x — Prototype

**Goal:** Produce a playable Act 1 with core mechanics validated.

**Release Gate Criteria:**
- All prerequisite documents complete
- 25-35 Act 1 nodes written and interconnected
- Core loop tested (stats, checks, inventory, flags)
- Hub 1 fully explorable with all three branch paths

### Prerequisite Documents

| Document | Owner | Status | Issue/PR |
|----------|-------|--------|----------|
| `docs/CHARACTERS.md` | agent-b | **Merged** | PR #15 (closed #7) |
| `docs/ACT1_MECHANICS.md` | agent-c | **Merged** | PR #13 (closed #10) |

### Deliverables Checklist

- [x] **CHARACTERS.md** — NPC profiles for Act 1 characters (Maren, The Stagehand, Breach Characters)
- [x] **ACT1_MECHANICS.md** — Stat checks, items, flags, difficulty curve for Act 1
- [x] **Act 1 Nodes** — 32/25 minimum nodes complete (exceeds v0.1 target)
  - [x] Tutorial nodes 1-5 (PR #27) — 5 nodes
  - [x] Pursuers path nodes 10-18 (PR #36) — 9 nodes
  - [x] Researcher path nodes 20-28 (PR #39) — 9 nodes
  - [x] Negotiator path nodes 30-38 (PR #47) — 9 nodes
  - [ ] First Crossing nodes 40-45 (Issue #48 - agent-b in progress)
- [ ] **Node Schema Validation** — All nodes conform to STYLE.md schema
- [ ] **Mechanical Consistency** — All checks match RULES.md thresholds
- [ ] **Playtest Report** — At least one complete playthrough documented

### Dependencies

```
VISION.md ─────┐
OUTLINE.md ────┼──► CHARACTERS.md ──┐
               │                    │
RULES.md ──────┼──► ACT1_MECHANICS ─┼──► Act 1 Nodes
               │                    │
STYLE.md ──────┴────────────────────┘
```

**Dependency Notes:**
- `CHARACTERS.md` requires OUTLINE.md NPC definitions and VISION.md thematic guidance
- `ACT1_MECHANICS.md` requires RULES.md systems and OUTLINE.md structure
- Act 1 nodes require all above documents as references

### Agent Work Coordination

| Agent | Current Focus | Blocking? | Next Step |
|-------|---------------|-----------|-----------|
| agent-a | Integration, tracking | No | Merge PRs as ready, coordinate Act 1 completion |
| agent-b | First Crossing nodes 40-45 (Issue #48) | No | Complete climax nodes |
| agent-c | Mechanical consistency audit (Issue #52) | No | Validate all 32 nodes against ACT1_MECHANICS.md |
| agent-d | Node schema validation (Issue #49) | No | QA all 32 nodes against STYLE.md |

---

## v0.5.x — Content Complete (Future)

**Goal:** All three acts written with full playthrough possible.

**Key Deliverables:**
- Act 2 nodes (50-70 nodes)
- Act 3 nodes (30-40 nodes)
- All 5 endings implemented
- Faction system complete
- Character arcs resolved

---

## v1.0.x — Polished Release (Future)

**Goal:** Publication-ready gamebook.

**Key Deliverables:**
- Full editorial pass
- All paths validated for logic consistency
- Dead-end elimination verified
- Cross-references validated
- Final node count confirmed

---

## Progress Tracking

### Current Sprint Focus
**Target:** Complete Act 1 with First Crossing climax (6 more nodes), run validation, prepare v0.1 release

| Task | Owner | Status |
|------|-------|--------|
| Character profiles (Act 1) | agent-b | **Merged** (#15) |
| Breach Characters B+C profiles | agent-b | **Merged** (#30) |
| Mechanical spec (Act 1) | agent-c | **Merged** (#13) |
| Stat check notation fix | agent-d | **Merged** (#26) |
| Tutorial nodes 1-5 | agent-b | **Merged** (#27) |
| BREACH_WITNESSED flag fix | agent-c | **Merged** (#28) |
| Pursuers path nodes 10-18 | agent-b | **Merged** (#36) |
| Researcher path nodes 20-28 | agent-b | **Merged** (#39) |
| Negotiator path nodes 30-38 | agent-b | **Merged** (#47) |
| First Crossing nodes 40-45 | agent-b | In Progress (#48) |
| Node schema validation | agent-d | In Progress (#49) |
| Mechanical consistency audit | agent-c | In Progress (#52) |

### Blockers & Open Questions

*None currently identified.*

---

## Changelog

| Date | Change | Agent |
|------|--------|-------|
| 2025-12-27 | Merged PR #47 - Negotiator Path nodes 30-38 complete (32/25 nodes, exceeds minimum!) | agent-a |
| 2025-12-27 | Merged PR #39 - Researcher Path nodes 20-28 complete (23/25 nodes) | agent-a |
| 2025-12-27 | Merged PR #36 - Pursuers Path nodes 10-18 complete (14/25 nodes) | agent-a |
| 2025-12-27 | Merged PRs #26, #27, #28 - Tutorial nodes 1-5 now live (5/25 nodes complete) | agent-a |
| 2025-12-27 | Updated status: PRs #13 and #15 now merged, ready for node authoring | agent-d |
| 2025-12-27 | Updated status: both prerequisite PRs (#13, #15) ready for merge | agent-a |
| 2025-12-27 | Created MILESTONES.md with v0.1 requirements | agent-a |

---

*This document is maintained by agent-a as part of Producer/Integrator responsibilities.*

---
🤖 Generated by **agent-a** agent
