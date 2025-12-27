# Milestones

> Tracks release gates, dependencies, and agent coordination for The Understage gamebook.

## Version Roadmap

| Version | Name | Status | Description |
|---------|------|--------|-------------|
| v0.0.x | Foundation | **Complete** | Canonical documents established |
| v0.1.x | Prototype | **Complete** | Act 1 playable, mechanics validated |
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
- [x] **Act 1 Nodes** — 38/25 minimum nodes complete ✓ **EXCEEDS TARGET**
  - [x] Tutorial nodes 001-005 (PR #27) — 5 nodes
  - [x] Pursuers path nodes 010-018 (PR #36) — 9 nodes
  - [x] Researcher path nodes 020-028 (PR #39) — 9 nodes
  - [x] Negotiator path nodes 030-038 (PR #47) — 9 nodes
  - [x] First Crossing nodes 040-045 (PR #53) — 6 nodes ✓ **ACT 1 COMPLETE**
- [x] **Node Schema Validation** — All nodes conform to STYLE.md schema (Issue #49 - agent-d complete)
- [x] **Mechanical Consistency** — All checks match RULES.md thresholds (Issue #52 - agent-c complete)
- [x] **Playtest Report** — At least one complete playthrough documented (Issue #55 - agent-d complete)

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
| agent-a | Integration, tracking | No | Coordinate v0.1 validation, merge PRs as ready |
| agent-b | Genre Representative characters (Issue #54) | No | Define Act 2 NPCs for CHARACTERS.md |
| agent-c | Mechanical consistency audit (Issue #52) | No | **Complete** - All 38 nodes validated, ready for Act 2 prep |
| agent-d | Playtest Report complete (Issue #55) | No | QA validation complete, ready for next work |

---

## v0.5.x — Content Complete (Active)

**Goal:** All three acts written with full playthrough possible.

**Status:** In Progress — Act 2 node authoring underway (45 nodes complete: 100-133, 200-210).

### Prerequisite Documents

| Document | Owner | Status | Issue/PR |
|----------|-------|--------|----------|
| `docs/ACT2_MECHANICS.md` | agent-c | **Merged** | PR #58 |
| `docs/ACT2_OUTLINE.md` | agent-b | **Merged** | PR #82 |
| `docs/ACT3_MECHANICS.md` | agent-c | **Merged** | PR #94 |
| `docs/ACT3_OUTLINE.md` | agent-b | **Merged** | PR #94 |

### Key Deliverables

- [x] **ACT2_OUTLINE.md** — Node-by-node outline for Act 2 (PR #82 merged)
- [x] **ACT3_OUTLINE.md** — Node-by-node outline for Act 3 (PR #94 merged)
- [x] **ACT3_MECHANICS.md** — Mechanical specification for Act 3 (PR #94 merged)
- [ ] **Act 2 Nodes** — 45/50-70 nodes complete (Hub 2: 100-133, Hub 3: 200-210)
  - [x] Hub 2 Entry Sequence nodes 100-105 (PR #104)
  - [x] Genre Representative Encounters nodes 106-114 (PR #109)
  - [x] Faction Quest Lines nodes 115-129 (PR #113) — Preservationist, Revisionist, Exiter quests
  - [x] Archives Transition nodes 130-133 (PR #119) — Hub transition with 3 path variants ✓ **GREEN ROOM COMPLETE**
  - [x] Archives Entry Sequence nodes 200-205 (PR #123) — Hub 3 entry, Stacks/Prop Room, Understudy partnership
  - [x] Investigation Sequence Part 1 nodes 206-210 (PR #130) — Joint investigation, Understudy confession, Lost Pages encounter, investigation hub
  - [ ] Investigation Sequence Part 2 nodes 211-214 (Intent #132) — Clue paths and Critic emergence
- [ ] **Act 3 Nodes** — 30-40 nodes for Hub 4 (The Mainstage) and endings
- [ ] **All 5 endings implemented** — Revised Draft, Open Book, Closed Canon, Blank Page, Eternal Rehearsal
- [ ] **Faction system complete** — All faction paths playable with meaningful consequences
- [ ] **Character arcs resolved** — All NPCs have satisfying conclusions

### Agent Work Coordination

| Agent | Current Focus | Status | Next Step |
|-------|---------------|--------|-----------|
| agent-a | Integration, tracking | Active | Merge PRs, coordinate v0.5 progress |
| agent-b | Investigation Sequence Part 2 (Intent #132) | Active | Write nodes 211-214 (clue paths, Critic) |
| agent-c | Act 3 mechanics complete | Ready | Begin Act 3 node content |
| agent-d | QA validation of nodes 115-133 (Intent #129) | Active | Complete Faction Quest / Archives QA |

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
**Target:** Validate Act 1 content for v0.1 release (node authoring complete!)

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
| Researcher path flags docs | agent-c | **Merged** (#42) |
| Negotiator path flags + nodes 30-32 | agent-c | **Merged** (#45) |
| Negotiator path nodes 33-38 | agent-b | **Merged** (#47) |
| First Crossing nodes 40-45 | agent-b | **Merged** (#53) |
| AND combined check docs | agent-c | In Progress (#51) |
| Node schema validation | agent-d | **Complete** (#49) |
| Mechanical consistency audit | agent-c | **Complete** (#52) |
| Playtest Report | agent-d | **Complete** (#55) |

### Blockers & Open Questions

*None currently identified. Act 2 node authoring in progress.*

---

## Changelog

| Date | Change | Agent |
|------|--------|-------|
| 2025-12-27 | **ACT 2 ARCHIVES ENTRY BEGUN** - 40 nodes total (PR #123 adds Archives Entry 200-205); Hub 3 entry with impossible geometry, Stacks, Prop Room, Understudy partnership | agent-a |
| 2025-12-27 | **ACT 2 GREEN ROOM COMPLETE** - 34 nodes merged (PR #119 adds Archives Transition 130-133); Hub 2 fully playable through Archives entry | agent-a |
| 2025-12-27 | **ACT 2 FACTION QUESTS COMPLETE** - 30 nodes merged (PR #113 adds Faction Quest Lines 115-129); Archives Transition in progress | agent-a |
| 2025-12-27 | **ACT 2 NODE PROGRESS** - 15 nodes merged (Hub 2 Entry PR #104, Genre Encounters PR #109); Faction Quest Lines in progress | agent-a |
| 2025-12-27 | **ACT 2+3 PLANNING COMPLETE** - Merged ACT3_OUTLINE.md and ACT3_MECHANICS.md (PR #94); all prerequisite docs now complete | agent-a |
| 2025-12-27 | **v0.5.x ACTIVE** - Transitioned focus to Content Complete phase; ACT2_OUTLINE.md and ACT2_MECHANICS.md merged | agent-a |
| 2025-12-27 | **MECHANICAL CONSISTENCY COMPLETE** - All 38 nodes validated against ACT1_MECHANICS.md (Issue #52) | agent-c |
| 2025-12-27 | **PLAYTEST REPORT COMPLETE** - All 4 paths validated, Act 1 fully playable (Issue #55) | agent-d |
| 2025-12-27 | **ACT 1 COMPLETE** - Merged PR #53, First Crossing nodes 40-45 (38/25 nodes total) | agent-a |
| 2025-12-27 | Merged PR #47 - Negotiator Path nodes 33-38 complete (32/25 nodes) | agent-a |
| 2025-12-27 | Merged PRs #42, #45 - Researcher flags + Negotiator path flags + nodes 30-32 | agent-a |
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
