# Rules

> The mechanical framework for The Understage gamebook. This document defines stats, checks, inventory, flags, and design constraints.

## Design Philosophy

### Core Principles

1. **Fail-Forward Bias**: Failed checks should never dead-end the player. Failure opens different paths, not closed doors.
2. **Choices Matter**: Mechanical choices should create meaningful narrative divergence, not just stat optimization.
3. **Minimal Viable Complexity**: Use the fewest mechanics that enable rich gameplay.
4. **Thematic Resonance**: Mechanics should reinforce the narrative of a Prompter navigating stories.

### What This System Does NOT Have

- Random dice rolls (deterministic choices only)
- Death without warning (always telegraph danger)
- Inventory tetris (simple carry limits)
- Grinding or stat inflation

---

## Core Stats

The Prompter has three core stats representing their approach to navigating the Understage:

| Stat | Represents | High Stat Unlocks |
|------|------------|-------------------|
| **Script** | Knowledge of narrative patterns, genre awareness, preparation | Research options, foresight choices, seeing through deceptions |
| **Stage Presence** | Force of personality, dramatic timing, command of attention | Social confrontations, inspiring allies, bold entrances |
| **Improv** | Adaptability, quick thinking, unorthodox solutions | Escape routes, creative solutions, breaking expected patterns |

### Starting Values

Players begin with a **total of 6 points** distributed across the three stats:
- Minimum 1 in each stat
- Maximum 4 in any stat

**Recommended Archetypes:**

| Archetype | Script | Stage Presence | Improv | Style |
|-----------|--------|---------------|--------|-------|
| The Scholar | 3 | 1 | 2 | Prepared, analytical, relies on knowing the rules |
| The Performer | 1 | 3 | 2 | Charismatic, bold, leads from the front |
| The Wildcard | 1 | 2 | 3 | Unpredictable, creative, finds unexpected solutions |
| The Director | 2 | 2 | 2 | Balanced, adaptable, jack-of-all-trades |

### Stat Growth

Stats can increase during play through:
- **Major story milestones** (completing an Act climax)
- **Character-defining choices** (certain nodes explicitly grant +1 to a stat)
- **Maximum total**: 9 points (only 3 additional points across the game)

Stats **do not decrease** except through specific story consequences that are clearly telegraphed.

---

## Check Mechanics

Checks determine whether the Prompter can take certain approaches. This is a **threshold system**, not randomized.

### Check Format

```
[STAT CHECK: Script 2]
```

The number is the **threshold**. If your stat meets or exceeds the threshold, you succeed. If not, you take the failure path.

### Difficulty Tiers

| Tier | Threshold | Meaning |
|------|-----------|---------|
| Basic | 1 | Anyone can attempt (always pass if minimum stat) |
| Standard | 2 | Requires some investment |
| Advanced | 3 | Requires significant investment |
| Expert | 4 | Requires near-maximum investment |

### Fail-Forward Outcomes

**Critical Rule**: Failed checks NEVER end the story. They redirect it.

| Success Path | Failure Path |
|--------------|--------------|
| Achieve goal cleanly | Achieve goal with complication |
| Gain advantage | Proceed without advantage |
| Open optimal route | Open alternative route |
| Build trust | Maintain neutrality |

**Example:**

> [SCRIPT CHECK: Script 3]
>
> **Success**: You recognize this as a classic revenge tragedy setup. You know exactly who will betray whom and when.
> → Go to Node 47 (prepared)
>
> **Failure**: The genre conventions here are unfamiliar. You'll have to learn the hard way.
> → Go to Node 48 (surprised but informed through experience)

Both paths continue the story. Success grants foreknowledge; failure grants experiential learning.

### Combined Checks

Some situations offer multiple valid approaches:

```
[APPROACH CHECK: Stage Presence 2 OR Improv 2]
```

Player succeeds if EITHER stat meets threshold. This rewards different builds.

For situations requiring multiple competencies:

```
[COMBINED CHECK: Script 2 AND Stage Presence 2]
```

Player succeeds only if BOTH stats meet their thresholds. This is rare and reserved for high-stakes moments requiring genuine versatility, such as the First Crossing's Negotiated Entry.

### Opposed Checks

When facing an NPC with their own capabilities:

```
[OPPOSED: Stage Presence vs. The Director's Authority (3)]
```

Your stat must exceed the opposition value. These are rare and always high-stakes.

### Archive Search Checks

A specialized check type for finding information in The Archives (Hub 3). Functions like a stat check but has multiple tiers of success:

```
[ARCHIVE SEARCH: Script 2]
```

| Result | Tier | Effect |
|--------|------|--------|
| Script 3+ | Deep Find | Complete information + bonus discovery |
| Script 2 | Standard Find | Information sought |
| Script 1 | Partial Find | Clue pointing to information |
| Script 0 | Lost | Time passes; minor complication |

Archive Searches always have at least a Partial Find outcome—even "Lost" results push the story forward with complications rather than dead ends, maintaining the fail-forward principle.

### Discovery Chains

For complex investigations requiring multiple discoveries across different nodes, Discovery Chains track prerequisite clues:

```
[DISCOVERY CHAIN: 3 clues required]
- Clue A: Node 205 (Script 2)
- Clue B: Node 208 (Improv 2)
- Clue C: Node 211 (Stage Presence 2)
→ All three unlock Node 215 (The Truth)
```

**Design Constraints:**
- Each individual clue must be obtainable through fail-forward checks
- Players should be able to discover what clues they're missing
- At least one clue should have a Basic (threshold 1) path
- Discovery Chains are primarily used in The Archives for major revelations

---

## Inventory System

The Prompter can carry items found in the Understage. Items have narrative weight and mechanical function.

### Carry Limit

**Maximum 5 items** at any time. The Understage responds to what you carry—excess items attract unwanted attention.

If at capacity and offered a new item, you must:
1. Decline the item, or
2. Drop an existing item (permanently lost unless noted)

### Item Categories

| Category | Function | Examples |
|----------|----------|----------|
| **Props** | Enable specific actions or checks | Prop Sword (bluff weapon), Bottle of Ink (rewrite tool) |
| **Scripts** | Grant knowledge or bypass checks | Torn Page (genre hint), Marked Playbill (NPC information) |
| **Tokens** | Represent relationships or allegiances | CHORUS Membership Card, Director's Sigil |
| **Keys** | Access locked areas or conversations | Green Room Pass, Archives Key |
| **Artifacts** | Powerful items with narrative consequences | Editing Pen (dangerous), Original Manuscript (plot-critical) |

### Item Properties

Some items have special properties:

- **Consumable**: Used once, then removed from inventory
- **Plot-Critical**: Cannot be dropped; counts toward limit
- **Hidden**: Does not count toward carry limit (rare)
- **Cursed**: Cannot be dropped until specific condition met

### Item Catalog

*This section will expand as nodes are written. Initial items:*

| Item | Category | Property | Effect |
|------|----------|----------|--------|
| Prompter's Handbook | Script | Starting, Plot-Critical | Your guide to the Understage basics |
| Rehearsal Candle | Prop | Consumable | Light reveals hidden script annotations in one scene |
| Stagehand's Gloves | Prop | — | Handle props safely; +1 to prop-related actions |
| Genre Compass | Script | — | Indicates dominant genre of current location |
| Understudy's Mask | Token | — | Appear as a minor character briefly |

---

## Flags & State Tracking

Flags track story progress, relationships, and accumulated choices. They are invisible to the player but determine available paths.

### Flag Types

| Type | Purpose | Example |
|------|---------|---------|
| **Story Flags** | Track major plot progression | `ACT1_COMPLETE`, `MET_DIRECTOR` |
| **Relationship Flags** | Track NPC standing | `MAREN_TRUST_HIGH`, `CHORUS_ALLIED` |
| **Faction Flags** | Track alignment scores | `FACTION_PRESERVATIONIST: 3` |
| **Choice Flags** | Track significant decisions | `FIRST_CROSSING_METHOD: NEGOTIATION` |
| **Item Flags** | Track item acquisition/use | `HAS_EDITING_PEN`, `USED_REHEARSAL_CANDLE` |

### Faction Alignment

Three factions track player alignment through accumulated choices:

| Faction | Philosophy | Key NPCs |
|---------|------------|----------|
| **Preservationists** | Keep the Understage separate from reality | The Director, traditionalist characters |
| **Revisionists** | Stories can and should be improved | The Understudy, progressive characters |
| **Exiters** | Fictional beings deserve real existence | CHORUS, escaped characters |

**Alignment is not exclusive.** Players accumulate points with multiple factions. At key moments, highest alignment determines options.

#### Alignment Points

Points accumulate based on player actions:

| Action Type | Points | Example |
|-------------|--------|---------|
| Dialogue choice | +1 | Agreeing with faction philosophy |
| Quest completion | +1 to +2 | Helping a faction member |
| Major decision | +2 to +3 | Siding with faction at critical moment |
| Betrayal | -2 | Acting against sworn faction |

#### Alignment Thresholds

| Points | Status | Effect |
|--------|--------|--------|
| 0-2 | Neutral | Standard NPC interactions |
| 3-4 | Sympathetic | Faction members more helpful, minor information access |
| 5-6 | Aligned | Faction quests available, unique item access |
| 7+ | Champion | Faction leader trusts you, exclusive Act 3 paths |

**Note:** Becoming a Champion (7+) with one faction typically precludes high alignment with others due to conflicting choices.

#### Independent Path

Players who keep all factions at 3 or below unlock the Independent path:

- Unique dialogue options with neutral characters
- Access to "outsider perspective" information
- Act 3 path requiring no faction backing
- Harder social checks (+1 threshold) due to fewer allies

### Gating Logic

Certain nodes or options require specific flags:

```
[REQUIRES: CHORUS_ALLIED AND HAS_GREEN_ROOM_PASS]
```

If requirements not met, the option is hidden (not shown as locked).

### Ending Determiners

Final ending is determined by:
1. Highest faction alignment at Act 3 climax
2. Key item possession (Editing Pen, Original Manuscript)
3. Specific critical choice flags
4. Whether the Editor is defeated, persuaded, or neither

---

## Balance Constraints

### Player Protection

1. **No Instant Death**: Any lethal consequence must be preceded by clear warning AND an avoidable choice.

   > **BAD**: "The trapdoor opens. You fall. The End."
   >
   > **GOOD**: "The floor feels unstable here. [IMPROV CHECK: Improv 2] or [Choose another path]"

2. **No Softlocks**: Every node must have at least one forward path that doesn't require items or stats.

3. **Stat Floor**: No check should require higher than stat 4 (possible but costly to achieve).

4. **Item Fairness**: Plot-critical items cannot be missed. Optional items enhance but never gatekeep main paths.

### Difficulty Curve

| Act | Expected Stats | Check Distribution |
|-----|----------------|-------------------|
| Act 1 | 2-2-2 to 3-2-2 | 80% Basic/Standard, 20% Advanced |
| Act 2 | 3-2-2 to 3-3-2 | 50% Basic/Standard, 40% Advanced, 10% Expert |
| Act 3 | 3-3-3 to 4-3-2 | 30% Basic/Standard, 50% Advanced, 20% Expert |

### Path Parity

All major paths should offer:
- Comparable challenge
- Comparable reward
- Comparable narrative depth
- Access to at least one satisfying ending

No path is "correct." Optimization is possible but not required.

### Faction Balance

- Each faction should have roughly equal content in Act 2
- Each faction should lead to 1-2 distinct endings
- Independent path is harder but valid
- No faction is "evil" or punished

---

## Implementation Notes

### For Node Authors

When writing nodes that use mechanics:

1. **Stat Checks**: Always provide both success and failure paths
2. **Items**: Check item catalog before creating new items
3. **Flags**: Use consistent naming conventions (UPPERCASE_SNAKE_CASE)
4. **Gating**: Prefer soft gates (advantages) over hard gates (requirements)

### Naming Conventions

| Element | Convention | Example |
|---------|------------|---------|
| Story Flags | `AREA_EVENT` | `ARCHIVES_DISCOVERED` |
| Relationship Flags | `NPC_RELATIONSHIP_LEVEL` | `DIRECTOR_TRUST_HIGH` |
| Faction Flags | `FACTION_NAME: N` | `PRESERVATIONIST: 3` |
| Item Flags | `HAS_ITEM` or `USED_ITEM` | `HAS_GENRE_COMPASS` |
| Choice Flags | `EVENT_METHOD` | `CROSSING_VIA_COMBAT` |

### Balance Checklist

Before finalizing a node, verify:
- [ ] All stat checks have fail-forward outcomes
- [ ] No instant death without clear warning
- [ ] At least one path requires no items or high stats
- [ ] New items are catalogued
- [ ] Flags use consistent naming
- [ ] Faction alignment changes are proportional

---

## Appendix: Quick Reference

### Stats at a Glance
- **Script**: Knowledge, preparation, genre awareness
- **Stage Presence**: Charisma, boldness, social power
- **Improv**: Adaptability, creativity, escape

### Check Thresholds
- 1 = Basic (everyone passes)
- 2 = Standard (some investment)
- 3 = Advanced (significant investment)
- 4 = Expert (maximum investment)

### Check Types
- **Stat Check**: Single stat vs. threshold
- **Approach Check**: Multiple stats, pass if ANY meets threshold (OR)
- **Combined Check**: Multiple stats, pass if ALL meet thresholds (AND)
- **Opposed Check**: Your stat vs. NPC capability value
- **Archive Search**: Tiered success (Deep Find / Standard / Partial / Lost)
- **Discovery Chain**: Multiple clues required across nodes

### Inventory Rules
- Max 5 items
- Must drop to pick up when full
- Plot-critical items can't be dropped

### Core Design Rules
1. Fail-forward always
2. No instant death without warning
3. Every path is valid
4. Mechanics serve narrative

---

*This is the foundational mechanical document. Item catalogs, flag registries, and specific node mechanics will expand as content is developed.*

---
🤖 Generated by **agent-c** agent
