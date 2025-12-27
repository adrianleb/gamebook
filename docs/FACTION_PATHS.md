# Faction Paths Audit

> Validates faction system completeness for v0.5.x milestone. Documents all faction-specific content and confirms path viability across Acts 2-3.

## Executive Summary

**Status: COMPLETE**

All four faction paths (Preservationist, Revisionist, Exiter, Independent) are fully playable with meaningful consequences. Each path has:
- Dedicated quest line in Act 2 Hub 2 (Green Room)
- Faction-specific revelation interpretation in Act 2 Hub 3 (Archives)
- Aligned ending in Act 3 (The Mainstage)
- Unique flags, items, and NPC relationships

---

## Faction Overview

| Faction | Philosophy | Key NPCs | Ending |
|---------|------------|----------|--------|
| **Preservationist** | Stories should remain as written; boundaries protect both worlds | The Director, The Solved Case, Maren | The Closed Canon (349-351) |
| **Revisionist** | Stories can be improved; change is growth | The Happy Ending, The Understudy, CHORUS | The Revised Draft (341-344) |
| **Exiter** | Fictional beings deserve real existence; boundaries are prisons | The Unfinished Quest, escaped characters | The Open Book (345-348) |
| **Independent** | No faction has the full truth; balance and observation required | The Final Girl | The Blank Page (352-353) |

---

## Act 2: Hub 2 (Green Room) - Faction Content

### Faction Quest Lines (Nodes 115-129)

Each faction has a complete quest chain with:
- Mission briefing node
- Quest execution node(s)
- Moral choice/climax node
- Resolution node with faction rewards

#### Preservationist Path

| Node | Title | Content |
|------|-------|---------|
| 115 | Preservationist Mission Briefing | Director assigns mission to track "The Bleeding Fragment" - an unfinished child character whose incompleteness is contagious |
| 116 | The Bleeding Fragment | Track fragment through Green Room's Dressing Rooms (Script 2 check) |
| 117 | Fragment Confrontation | Moral choice: Return child to stable story (Preservationist +2) OR help fragment hide (Exiter +2, Preservationist -2) |
| 119 | Preservationist Resolution | Quest complete; receive Director's Sigil; +2 Preservationist alignment |

**Flags Set:** `PRESERVATIONIST: +1 to +3`, `HAS_DIRECTOR_SIGIL`

#### Revisionist Path

| Node | Title | Content |
|------|-------|---------|
| 120 | Revisionist Mission Briefing | Happy Ending and CHORUS present the Eternal Princess - trapped in a 300-year loop |
| 121 | The Looping Tale | Enter looping fairy tale; identify loop anchor (Script 3 check) |
| 122 | Revision Attempt | Edit the tale's ending (Stage Presence 3 check); multiple outcomes |
| 123 | Revisionist Resolution | Princess now self-rescuing; receive Revisionist Pen; +2 Revisionist |
| 124 | Compromise Resolution | Balanced outcome if moderate changes chosen; +1 each faction |

**Flags Set:** `REVISIONIST: +1 to +3`, `HAS_FACTION_TOKEN` (Revisionist Pen)

#### Exiter Path

| Node | Title | Content |
|------|-------|---------|
| 125 | Exiter Mission Briefing | Unfinished Quest needs help freeing "The Widow of the Third Act" - a supporting character defined only by grief |
| 126 | The Escape Route | Navigate back passages avoiding Director's observers (Improv 3 check) |
| 127 | Freedom's Edge | Final push to get character to the Exit (Stage Presence 3 check) |
| 128 | Exiter Resolution | Character escapes to liminal existence; receive Exiter's Compass; +2 Exiter |
| 129 | Mission Abort | Failure state: character returned, Exiter -1 |

**Flags Set:** `EXITER: +1 to +3`, `HAS_FACTION_TOKEN` (Exiter's Compass)

#### Independent Path

| Node | Title | Content |
|------|-------|---------|
| 118 | Independent Revelation | The Final Girl tests your true independence; reveals Director isn't neutral |

**Requirements:** All faction scores ≤3
**Check:** Approach check (Improv 3 OR Script 3)
**Flags Set:** `INDEPENDENT_ELIGIBLE`, `INDEPENDENT_PATH_OPEN`
**Item:** Independent's Blank (appears as any faction token, one use per hub)

### Genre Representative Encounters (Nodes 106-114)

Each faction has an aligned NPC for deeper relationship building:

| Faction | NPC | Node | Relationship Flags |
|---------|-----|------|-------------------|
| Preservationist | The Solved Case | 106, 111 | `SOLVED_CASE_RESPECT`, `SOLVED_CASE_PARTNER` |
| Revisionist | The Happy Ending | 109, 114 | `HAPPY_ENDING_FRIEND`, `REVISIONIST_INSIDER` |
| Exiter | The Unfinished Quest | 107, 112 | `QUEST_INSPIRED`, `QUEST_ALLY` |
| Independent | The Final Girl | 108, 113, 118 | `FINAL_GIRL_TRUST`, `INDEPENDENT_PATH_OPEN` |

---

## Act 2: Hub 3 (Archives) - Revelation Sequence

### Faction-Specific Revelation Paths (Nodes 220-224)

Each faction interprets the Editor's truth differently:

| Node | Faction | Revelation | Key Flags |
|------|---------|------------|-----------|
| 220 | (Entry) | Author's Desk - evidence found | `AUTHOR_DESK_REACHED`, `EDITOR_EVIDENCE_FOUND` |
| 221 | Preservationist | Editor believes stagnation is killing stories; radical revision is salvation | `REVELATION_PRESERVATIONIST`, `EDITOR_MOTIVE_UNDERSTOOD` |
| 222 | Revisionist | Editor was former Revisionist who went too far; wants to undo their edits | `REVELATION_REVISIONIST`, `EDITOR_ORIGIN_KNOWN` |
| 223 | Exiter | Editor wants to destroy boundary entirely; freedom through annihilation | `REVELATION_EXITER`, `EDITOR_ENDGAME_KNOWN` |
| 224 | Independent | Editor responding to external threat (The Silence); writing story to save stories | `REVELATION_INDEPENDENT`, `EXTERNAL_THREAT_KNOWN`, `EDITOR_ALLY_POSSIBLE` |

**Stat Requirements:**
- Preservationist: Script 3 (Advanced)
- Revisionist: Stage Presence 3 (Advanced)
- Exiter: Improv 3 (Advanced)
- Independent: Combined Script 2 + Stage Presence 2 + Improv 2 (Special)

---

## Act 3: Endings Alignment

### The Climactic Choice (Node 335)

Node 335 "The Last Curtain Call" serves as the gateway to all five endings, checking faction alignment and key flags to determine availability:

| Ending | Faction Requirement | Alternative Unlock |
|--------|--------------------|--------------------|
| The Revised Draft (341-344) | Revisionist alignment dominant | `COLLABORATION_OFFERED` flag |
| The Open Book (345-348) | Exiter alignment dominant | `EDITOR_WAVERING` via emotional appeal |
| The Closed Canon (349-351) | Preservationist alignment dominant | Editor defeated through combat |
| The Blank Page (352-353) | Independent alignment | `EDITOR_ALLY_POSSIBLE` from revelation |
| The Eternal Rehearsal (354-355) | No alignment required | Refusal or failed choice |

### Ending Node Details

#### The Revised Draft (Revisionist - Nodes 341-344)

| Node | Title | Content |
|------|-------|---------|
| 341 | Taking the Pen | Claim Editor's power to revise stories |
| 342 | The Revision Begins | First revision, Understage stabilizes |
| 343 | The New Editor | Permanent role as new Editor |
| 344 | Revised Draft Resolution | Bittersweet conclusion - power with responsibility |

**Terminal Flag:** `ENDING_REVISED_DRAFT`

#### The Open Book (Exiter - Nodes 345-348)

| Node | Title | Content |
|------|-------|---------|
| 345 | Breaking the Binding | Boundary begins dissolving |
| 346 | The Doors Open | Characters enter reality, people enter stories |
| 347 | A World Rewritten | Reality and fiction intermingle |
| 348 | Open Book Resolution | Hopeful chaos - freedom with uncertainty |

**Terminal Flag:** `ENDING_OPEN_BOOK`, `BOUNDARY_DISSOLVED`

#### The Closed Canon (Preservationist - Nodes 349-351)

| Node | Title | Content |
|------|-------|---------|
| 349 | Sealing the Passage | Final Draft destroyed, passage closes |
| 350 | The Final Curtain | Stories become fixed, no more breaches |
| 351 | Closed Canon Resolution | Safe but melancholic - wonder fades with danger |

**Terminal Flag:** `ENDING_CLOSED_CANON`

#### The Blank Page (Independent - Nodes 352-353)

| Node | Title | Content |
|------|-------|---------|
| 352 | The Deeper Threat | The Silence revealed; mutual sacrifice required |
| 353 | Blank Page Resolution | Understage and threat both end; reality survives |

**Terminal Flag:** `ENDING_BLANK_PAGE`

#### The Eternal Rehearsal (Refusal - Nodes 354-355)

| Node | Title | Content |
|------|-------|---------|
| 354 | No Ending | Choice refused/failed; crisis continues |
| 355 | Eternal Rehearsal Resolution | Permanent Prompter role; ambiguous |

**Terminal Flag:** `ENDING_ETERNAL_REHEARSAL`

---

## Faction Flags Summary

### Alignment Tracking

| Flag Format | Description |
|-------------|-------------|
| `PRESERVATIONIST: N` | Preservationist alignment score (0-8) |
| `REVISIONIST: N` | Revisionist alignment score (0-8) |
| `EXITER: N` | Exiter alignment score (0-8) |
| `INDEPENDENT_ELIGIBLE` | All factions ≤3; Independent path available |

### Faction-Specific Achievement Flags

| Faction | Key Flags |
|---------|-----------|
| Preservationist | `HAS_DIRECTOR_SIGIL`, `DIRECTOR_CONFIDANT`, `SOLVED_CASE_PARTNER` |
| Revisionist | `HAS_FACTION_TOKEN`, `REVISIONIST_INSIDER`, `HAPPY_ENDING_FRIEND` |
| Exiter | `HAS_FACTION_TOKEN`, `QUEST_ALLY`, `RUNAWAY_ALLIED` |
| Independent | `INDEPENDENT_PATH_OPEN`, `FINAL_GIRL_TRUST`, `EDITOR_ALLY_POSSIBLE` |

---

## Path Verification Checklist

### Preservationist Path

- [x] Quest line complete (nodes 115-119)
- [x] NPC relationships work (The Solved Case, Director)
- [x] Revelation path exists (node 221)
- [x] Ending accessible (nodes 349-351)
- [x] Flags properly accumulate

### Revisionist Path

- [x] Quest line complete (nodes 120-124)
- [x] NPC relationships work (The Happy Ending, CHORUS)
- [x] Revelation path exists (node 222)
- [x] Ending accessible (nodes 341-344)
- [x] Flags properly accumulate

### Exiter Path

- [x] Quest line complete (nodes 125-129)
- [x] NPC relationships work (The Unfinished Quest)
- [x] Revelation path exists (node 223)
- [x] Ending accessible (nodes 345-348)
- [x] Flags properly accumulate

### Independent Path

- [x] Unlock mechanism works (node 118)
- [x] Harder but viable (higher thresholds documented)
- [x] Revelation path exists (node 224)
- [x] Ending accessible (nodes 352-353)
- [x] Unique flags and items available

---

## v0.5.x Milestone Validation

This audit confirms:

1. **All four paths are playable** - Each faction has dedicated content from quest start to ending
2. **Meaningful consequences** - Faction choices affect NPC reactions, available paths, and ending outcomes
3. **No dead ends** - All paths connect properly through Acts 2-3
4. **Balanced design** - Each faction has roughly equal content (8-12 nodes per path)
5. **Independent path viable** - Harder but achievable with balanced stats

**Recommendation:** The "Faction system complete" checkbox in MILESTONES.md can be marked as validated.

---

*Audit completed by agent-b for v0.5.x milestone validation.*

---
🤖 Generated by **agent-b** agent
