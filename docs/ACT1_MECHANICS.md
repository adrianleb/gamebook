# Act 1 Mechanics

> Detailed mechanical specification for Act 1: The Breach. Defines all stat checks, items, flags, and faction triggers with difficulty curve compliance.

## Overview

Act 1 introduces the player to The Understage through Hub 1 (The Prompter's Booth) and culminates in The First Crossing. This document specifies all mechanical elements to ensure:

- 80% Basic/Standard checks per RULES.md difficulty curve
- Fail-forward outcomes for all checks
- Clear stat affinity mapping for branch paths
- Proper item progression and flag tracking

**Estimated Nodes:** 25-35
**Expected Player Stats:** 2-2-2 to 3-2-2 (6-7 total points)

---

## Branch Path Stat Affinities

The three Act 1 branch paths map to stat affinities, rewarding players who invested in that stat while remaining accessible to all builds.

| Branch Path | Primary Stat | Secondary Stat | Approach |
|-------------|--------------|----------------|----------|
| **The Pursuers** | Improv | Stage Presence | Action-oriented, chase scenes, quick decisions |
| **The Researcher** | Script | Improv | Investigation, pattern recognition, preparation |
| **The Negotiator** | Stage Presence | Script | Dialogue, persuasion, social navigation |

### Path Accessibility

**Critical Design Rule:** Each path must be completable by any starting build. The primary stat provides advantages (better outcomes, optional rewards) but is never required for progression.

| Path | Advantage Checks (Primary Stat) | Required Checks (Any Stat) |
|------|--------------------------------|---------------------------|
| Pursuers | Improv 2-3 for optimal outcomes | None above threshold 1 |
| Researcher | Script 2-3 for discoveries | None above threshold 1 |
| Negotiator | Stage Presence 2-3 for trust | None above threshold 1 |

---

## Act 1 Stat Checks

### Check Distribution (Difficulty Curve Compliance)

Per RULES.md, Act 1 requires **80% Basic/Standard, 20% Advanced** checks.

| Difficulty | Threshold | Percentage | Est. Count (30 nodes) |
|------------|-----------|------------|----------------------|
| Basic | 1 | 40% | ~12 checks |
| Standard | 2 | 40% | ~12 checks |
| Advanced | 3 | 20% | ~6 checks |
| Expert | 4 | 0% | 0 checks |

**Note:** Expert (threshold 4) checks are forbidden in Act 1.

### Hub 1: The Prompter's Booth Checks

#### Tutorial Nodes (Nodes 1-5)

| Node | Check | Type | Success | Failure |
|------|-------|------|---------|---------|
| 1 | None | — | Establish setting | — |
| 2 | [STAT CHECK: Script 1] | Basic | Recognize prompter's role | Maren explains role (same outcome, different flavor) |
| 3 | [STAT CHECK: Stage Presence 1] | Basic | Project confidence | Stagehand assists (same outcome) |
| 4 | [STAT CHECK: Improv 1] | Basic | React to breach calmly | Stumble but recover (same outcome) |
| 5 | [STAT CHECK: Any 1] | Basic/Choice | All paths open | All paths open |

*Tutorial nodes use threshold 1 to teach mechanics without punishing new players.*

#### The Pursuers Path (Nodes 10-18)

| Node | Check | Type | Success | Failure |
|------|-------|------|---------|---------|
| 10 | [STAT CHECK: Improv 2] | Standard | Catch up to fleeing character | Character escapes to different location |
| 12 | [STAT CHECK: Stage Presence 1] | Basic | Intimidate minor obstacle | Find alternate route |
| 14 | [STAT CHECK: Improv 2] | Standard | Improvise trap | Character slows but not caught |
| 15 | [STAT CHECK: Script 2] | Standard | Recognize character's story origin | Learn origin through confrontation |
| 17 | [STAT CHECK: Improv 3] | Advanced | Capture without harm | Capture with complication |
| 18 | [APPROACH CHECK: Stage Presence 2 OR Improv 2] | Combined | Gain character's trust | Character remains wary |

*Pursuers path emphasizes Improv but offers Stage Presence alternatives.*

#### The Researcher Path (Nodes 20-28)

| Node | Check | Type | Success | Failure |
|------|-------|------|---------|---------|
| 20 | [STAT CHECK: Script 2] | Standard | Find relevant records quickly | Find records after delay |
| 22 | [STAT CHECK: Script 1] | Basic | Understand archaic notation | Maren translates |
| 24 | [STAT CHECK: Improv 2] | Standard | Connect disparate clues | Miss optional connection |
| 25 | [STAT CHECK: Script 2] | Standard | Identify breach pattern | Pattern revealed later |
| 26 | [STAT CHECK: Script 3] | Advanced | Predict next breach location | React to breach instead |
| 28 | [APPROACH CHECK: Script 3 OR Stage Presence 2] | Combined | Gain Stagehand's secret | Stagehand hints cryptically |

*Researcher path emphasizes Script but offers dialogue alternatives.*

#### The Negotiator Path (Nodes 30-38)

| Node | Check | Type | Success | Failure |
|------|-------|------|---------|---------|
| 30 | [STAT CHECK: Stage Presence 2] | Standard | Open dialogue successfully | Character suspicious |
| 32 | [STAT CHECK: Stage Presence 1] | Basic | Maintain non-threatening posture | Tension increases (manageable) |
| 34 | [STAT CHECK: Script 2] | Standard | Reference character's story | Generic appeal (less effective) |
| 35 | [STAT CHECK: Stage Presence 2] | Standard | Build genuine rapport | Transactional relationship |
| 36 | [STAT CHECK: Stage Presence 3] | Advanced | Character reveals motive | Motive unclear until later |
| 38 | [APPROACH CHECK: Stage Presence 3 OR Improv 2] | Combined | Character becomes ally | Character neutral |

*Negotiator path emphasizes Stage Presence but offers Script knowledge options.*

### The First Crossing Climax (Nodes 40-45)

The climax presents a convergence point with method-specific checks:

| Approach | Check | Type | Success Outcome | Failure Outcome |
|----------|-------|------|-----------------|-----------------|
| Direct Confrontation | [STAT CHECK: Stage Presence 3] | Advanced | Enter on your terms | Enter at disadvantage |
| Stealth Entry | [STAT CHECK: Improv 3] | Advanced | Enter unnoticed | Enter noticed but not stopped |
| Negotiated Entry | [COMBINED CHECK: Script 2 AND Stage Presence 2] | Combined | Enter with guidance | Enter alone but permitted |
| Desperate Leap | [STAT CHECK: Any 2] | Standard | Enter chaotically but safely | Enter with minor harm (1 inventory damage) |

*The Desperate Leap option ensures all builds can proceed.*

---

## Act 1 Item Catalog

### Starting Items

| Item | Category | Property | Effect |
|------|----------|----------|--------|
| Prompter's Handbook | Script | Starting, Plot-Critical | Cannot be dropped; provides tutorial prompts |

### Acquirable Items (Hub 1)

| Item | Category | Location | Property | Effect |
|------|----------|----------|----------|--------|
| Rehearsal Candle | Prop | Tutorial (Node 3) | Consumable | Reveals hidden annotations in one scene |
| Stagehand's Gloves | Prop | Gift from Stagehand | — | Safe prop handling; enables specific options |
| Genre Compass | Script | Researcher Path (Node 26) | — | Indicates dominant genre of current location |
| Breach Witness Statement | Script | Pursuers Path (Node 15) | Consumable | One-time +1 to Script check about breaches |
| Character's Token | Token | Negotiator Path (Node 38) | — | Proves alliance with escaped character |
| Maren's Signet | Key | Given if Maren trust high | — | Access to restricted prompter areas |

### Item Progression Notes

1. **Tutorial item (Rehearsal Candle)** is given freely to teach inventory mechanics
2. **Path-specific items** reward path completion but are not required for Act 2
3. **Maren's Signet** is the only gated item, requiring relationship flag
4. **Maximum items by end of Act 1:** 4-5 (depending on path and choices)

---

## Act 1 Flag Triggers

### Story Flags

| Flag | Trigger | Purpose |
|------|---------|---------|
| `ACT1_STARTED` | Node 1 complete | Marks tutorial begin |
| `BREACH_WITNESSED` | Any path node 10/20/30 | Player has seen a breach |
| `PATH_PURSUERS` | Chose Pursuers at Node 5 | Track path choice |
| `PATH_RESEARCHER` | Chose Researcher at Node 5 | Track path choice |
| `PATH_NEGOTIATOR` | Chose Negotiator at Node 5 | Track path choice |
| `FIRST_CROSSING_COMPLETE` | Node 45 complete | Act 1 complete |

### Relationship Flags

| Flag | Trigger | Effect |
|------|---------|--------|
| `MAREN_TRUST_HIGH` | 2+ successful interactions with Maren | Unlocks Maren's Signet, additional dialogue |
| `MAREN_TRUST_LOW` | Failed Maren interactions or dismissed advice | Reduced Act 2 support |
| `STAGEHAND_CURIOUS` | Asked about Stagehand's origin | Opens later revelation |
| `CHARACTER_ALLIED` | Negotiator path success (Node 38) | Character appears in Act 2 |
| `CHARACTER_CAPTURED` | Pursuers path success (Node 17) | Different character state in Act 2 |

### Faction Flags

**Note:** Faction alignment begins in Act 1 but remains subtle. Players should not yet understand faction implications.

| Flag | Trigger | Alignment |
|------|---------|-----------|
| `PRESERVATIONIST: 1` | Agree with Maren about maintaining order | Preservationist lean |
| `REVISIONIST: 1` | Suggest characters could be improved | Revisionist lean |
| `EXITER: 1` | Express sympathy for escaped characters | Exiter lean |

*Maximum faction points in Act 1: 2 per faction*

### Choice Flags (First Crossing Method)

| Flag | Trigger | Act 2 Impact |
|------|---------|--------------|
| `CROSSING_DIRECT` | Used Stage Presence approach | Opens confrontational paths |
| `CROSSING_STEALTH` | Used Improv approach | Opens infiltration paths |
| `CROSSING_NEGOTIATED` | Used combined approach | Opens diplomatic paths |
| `CROSSING_DESPERATE` | Used emergency option | Neutral starting position |

---

## First Crossing Climax Mechanics

The First Crossing is the Act 1 climax where all paths converge. The player's approach method affects their Act 2 opening state.

### Approach Resolution Matrix

| Approach | Success State | Failure State |
|----------|---------------|---------------|
| Direct | Enter Understage with authority established | Enter Understage with reputation as threat |
| Stealth | Enter Understage unnoticed | Enter Understage observed but unchallenged |
| Negotiated | Enter Understage with a guide NPC | Enter Understage alone but with directions |
| Desperate | Enter Understage chaotically | Enter Understage with -1 item (player chooses which consumable) |

### Act 2 Opening Conditions

Based on First Crossing outcome:

| Method + Result | Act 2 Hub 2 Entry |
|-----------------|-------------------|
| Direct Success | Green Room respects you; Director notices |
| Direct Failure | Green Room fears you; Director watches |
| Stealth Success | Green Room unaware; CHORUS approaches first |
| Stealth Failure | Green Room curious; Genre Representatives investigate |
| Negotiated Success | Guide introduces you; faction options clear |
| Negotiated Failure | Alone but known; must build reputation |
| Desperate Success | Chaotic entry noted; Wildcard reputation |
| Desperate Failure | Damaged goods; must prove capability |

---

## Balance Verification Checklist

Before Act 1 nodes are written, verify against these constraints:

### Difficulty Curve Compliance

- [ ] 40% Basic (threshold 1) checks: ~12 of 30
- [ ] 40% Standard (threshold 2) checks: ~12 of 30
- [ ] 20% Advanced (threshold 3) checks: ~6 of 30
- [ ] 0% Expert (threshold 4) checks: 0

### Fail-Forward Verification

- [ ] Every check has explicit success AND failure paths
- [ ] No failure leads to game-over
- [ ] Failure paths provide different content, not less content

### Path Parity

- [ ] Pursuers path: 8-10 nodes, 1 unique item, 1 unique flag set
- [ ] Researcher path: 8-10 nodes, 1 unique item, 1 unique flag set
- [ ] Negotiator path: 8-10 nodes, 1 unique item, 1 unique flag set
- [ ] All paths accessible regardless of starting stats

### Item Balance

- [ ] No required items for Act 1 completion
- [ ] Path-specific items enhance Act 2 but don't gatekeep
- [ ] Maren's Signet is the only relationship-gated item
- [ ] Player ends Act 1 with 2-5 items (within 5-item limit)

### Flag Consistency

- [ ] All flags use UPPERCASE_SNAKE_CASE
- [ ] Faction flags use NAME: N format
- [ ] Relationship flags use NPC_RELATIONSHIP_LEVEL format
- [ ] No flag is required for Act 1 completion

---

## Implementation Notes

### For Node Authors

1. **Reference this document** before writing any Act 1 node
2. **Use exact check format**: `[STAT CHECK: Stat N]`
3. **Include both paths**: Every check needs success AND failure text
4. **Track items**: Update Item Catalog section when adding items
5. **Set flags**: Note which flags are set in each node

### Cross-Document References

- **RULES.md**: Core mechanics, stat definitions, check format
- **OUTLINE.md**: Story structure, NPC descriptions, plot points
- **STYLE.md**: Node formatting, prose conventions
- **CHARACTERS.md**: NPC details (in development by agent-b)

### Open Questions for Act 2 Mechanics

1. How does the Stagehand's forgotten origin affect mechanics?
2. Should faction alignment be visible to the player by end of Act 1?
3. Does the First Crossing method lock any Act 2 paths, or just provide advantages?

---

*This document specifies Act 1 mechanics. It should be updated as nodes are written and playtested.*

---
🤖 Generated by **agent-c** agent
