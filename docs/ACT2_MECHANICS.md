# Act 2 Mechanics

> Detailed mechanical specification for Act 2: The Descent. Defines faction alignment system, stat checks, items, flags, and NPC interactions across Hub 2 (The Green Room) and Hub 3 (The Archives).

## Overview

Act 2 expands the Understage experience through two major hubs: the social-political Green Room where factions vie for influence, and the investigative Archives where truth lies buried. This document specifies all mechanical elements to ensure:

- 50% Basic/Standard, 40% Advanced, 10% Expert checks per RULES.md difficulty curve
- Fail-forward outcomes for all checks
- Faction alignment as the primary progression mechanic
- Clear NPC relationship tracking across 6+ new characters

**Estimated Nodes:** 50-70
**Expected Player Stats:** 3-2-2 to 3-3-2 (7-8 total points)
**Maximum Stat Growth:** +1 to any stat (from Act 1 climax or major Act 2 choice)

---

## Faction Alignment System

### Core Concept

Faction alignment is the central mechanic of Act 2. Player choices accumulate alignment points with three factions, determining available paths, NPC reactions, and ultimately Act 3 options.

### The Three Factions

| Faction | Philosophy | Key NPCs | Color Code |
|---------|------------|----------|------------|
| **Preservationists** | Stories should remain as written; the boundary protects both worlds | The Director, The Solved Case, Maren | Gold |
| **Revisionists** | Stories can be improved; change is growth, not destruction | The Happy Ending, The Understudy, CHORUS | Silver |
| **Exiters** | Fictional beings deserve real existence; the boundary is a prison | The Unfinished Quest, escaped characters, CHORUS (faction overlap) | Copper |

### Alignment Points

**Accumulation:**
- Dialogue choices: +1 to aligned faction
- Quest completion: +1 to +2 depending on approach
- Major decisions: +2 to +3 (rare, clearly signposted)
- Betraying a faction: -2 from betrayed faction

**Act 2 Thresholds:**

| Points | Status | Effect |
|--------|--------|--------|
| 0-2 | Neutral | Standard NPC interactions |
| 3-4 | Sympathetic | Faction members more helpful, minor information access |
| 5-6 | Aligned | Faction quests available, +1 item access |
| 7+ | Champion | Faction leader trusts you, exclusive Act 3 paths |

**Maximum Points per Faction in Act 2:** 8 (requires near-exclusive alignment)

### Independent Path

Players who keep all factions at 3 or below unlock the Independent path:
- Unique dialogue options with The Final Girl (fellow Independent)
- Access to "outsider perspective" information
- Act 3 path that requires no faction backing

**Difficulty:** Independent path has fewer allies and harder checks (threshold +1 on some social checks).

### Faction Consequences

| Situation | Preservationist | Revisionist | Exiter |
|-----------|-----------------|-------------|--------|
| **NPC in Danger** | Prioritize order; sacrifice may be necessary | Rewrite the situation; find loopholes | Free them regardless of consequences |
| **Disputed Territory** | Maintain boundaries as written | Negotiate new terms | Abolish the boundary entirely |
| **Story Fragment Found** | Return it to the Archives | Study it for improvement | Share it freely |

---

## Hub 2: The Green Room

### Overview

The Green Room is a neutral space where characters from different stories mingle. Social maneuvering, faction politics, and information gathering dominate.

**Key Locations:**
- The Main Lounge (central hub, faction representatives present)
- The Dressing Rooms (private conversations, relationship building)
- The Call Board (quest hooks, rumors, faction missions)

**Primary Stat Affinity:** Stage Presence
**Secondary Stat Affinity:** Script

### Green Room Check Distribution

Per RULES.md Act 2 curve (50% Basic/Standard, 40% Advanced, 10% Expert):

| Difficulty | Threshold | Percentage | Est. Count (25-35 nodes) |
|------------|-----------|------------|--------------------------|
| Basic | 1 | 25% | ~7-9 checks |
| Standard | 2 | 25% | ~7-9 checks |
| Advanced | 3 | 40% | ~10-14 checks |
| Expert | 4 | 10% | ~3-4 checks |

### NPC Interactions: The Director

**Stat Affinity:** Stage Presence (authority recognition) / Script (understanding their history)

| Node Range | Check | Type | Success | Failure |
|------------|-------|------|---------|---------|
| 100-102 | [STAT CHECK: Stage Presence 2] | Standard | Director acknowledges you as worthy of attention | Director dismisses you to underlings |
| 105-107 | [STAT CHECK: Script 3] | Advanced | Recognize Director's inconsistencies | Director's narrative accepted at face value |
| 110-112 | [OPPOSED: Stage Presence vs. Director's Authority (3)] | Opposed | Challenge Director's ruling successfully | Submit to Director's judgment |
| 115-118 | [STAT CHECK: Stage Presence 4] | Expert | Earn Director's private audience | Must earn trust through faction service first |

**Director Relationship Flags:**
- `DIRECTOR_IMPRESSED`: Made strong first impression; +1 to future social checks with Director
- `DIRECTOR_SUSPICIOUS`: Director watches you closely; some paths restricted
- `DIRECTOR_CONFIDANT`: Director shares private concerns; unlocks Revelation clues

### NPC Interactions: CHORUS

**Stat Affinity:** Improv (speaking their language) / Stage Presence (earning respect)

| Node Range | Check | Type | Success | Failure |
|------------|-------|------|---------|---------|
| 103-104 | [STAT CHECK: Improv 1] | Basic | CHORUS welcomes you; share minor information | CHORUS ignores you; must earn attention |
| 108-109 | [STAT CHECK: Stage Presence 2] | Standard | CHORUS shares useful rumor | Generic information only |
| 113-114 | [APPROACH CHECK: Improv 3 OR Stage Presence 3] | Combined | CHORUS reveals faction secrets | CHORUS hints cryptically |
| 120-122 | [STAT CHECK: Improv 3] | Advanced | Join CHORUS temporarily; access collective memory | CHORUS amused but unhelpful |

**CHORUS Relationship Flags:**
- `CHORUS_MEMBER`: Inducted into CHORUS; access to collective knowledge
- `CHORUS_ALLY`: Helped CHORUS; they owe you a favor
- `CHORUS_DISMISSED`: Offended CHORUS; information costs double (favor or item)

### NPC Interactions: Genre Representatives

#### The Solved Case (Preservationist)

**Stat Affinity:** Script (detective work) / Stage Presence (interrogation)

| Node Range | Check | Type | Success | Failure |
|------------|-------|------|---------|---------|
| 106 | [STAT CHECK: Script 2] | Standard | Present case logically; earn respect | Dismissed as amateur |
| 111 | [STAT CHECK: Script 3] | Advanced | Solve their puzzle; gain information | They solve it for you (no reward) |
| 116 | [OPPOSED: Script vs. Solved Case's Deduction (3)] | Opposed | Catch their deliberate error | Accept false conclusion |

**Flags:** `SOLVED_CASE_RESPECT`, `SOLVED_CASE_PARTNER` (working together on investigation)

#### The Unfinished Quest (Exiter)

**Stat Affinity:** Stage Presence (heroic presence) / Improv (unconventional thinking)

| Node Range | Check | Type | Success | Failure |
|------------|-------|------|---------|---------|
| 107 | [STAT CHECK: Stage Presence 2] | Standard | Recognized as fellow protagonist | Seen as supporting character |
| 112 | [STAT CHECK: Improv 2] | Standard | Suggest new narrative possibility | Offer only familiar tropes |
| 117 | [STAT CHECK: Stage Presence 3] | Advanced | Inspire them to action | They remain contemplative |

**Flags:** `QUEST_INSPIRED`, `QUEST_ALLY` (will join Act 3 confrontation)

#### The Final Girl (Independent)

**Stat Affinity:** Improv (survival instinct) / Script (pattern recognition)

| Node Range | Check | Type | Success | Failure |
|------------|-------|------|---------|---------|
| 108 | [STAT CHECK: Improv 2] | Standard | She shares survival wisdom | Generic advice only |
| 113 | [STAT CHECK: Script 2] | Standard | Recognize her pattern-breaking | Miss the significance |
| 118 | [APPROACH CHECK: Improv 3 OR Script 3] | Combined | She reveals the Director's secret | Hints only; must discover independently |

**Flags:** `FINAL_GIRL_TRUST`, `INDEPENDENT_PATH_OPEN` (if faction scores all low)

#### The Happy Ending (Revisionist)

**Stat Affinity:** Stage Presence (charm) / Script (narrative understanding)

| Node Range | Check | Type | Success | Failure |
|------------|-------|------|---------|---------|
| 109 | [STAT CHECK: Stage Presence 1] | Basic | Pleasant conversation; minor help | Polite but distant |
| 114 | [STAT CHECK: Script 3] | Advanced | Understand their revision philosophy | Simplistic understanding |
| 119 | [STAT CHECK: Stage Presence 3] | Advanced | They share authorial secrets | General Revisionist philosophy only |

**Flags:** `HAPPY_ENDING_FRIEND`, `REVISIONIST_INSIDER` (access to revision techniques)

---

## Hub 3: The Archives

### Overview

The Archives house forgotten stories, first drafts, and dangerous knowledge. Investigation and survival dominate here.

**Key Locations:**
- The Stacks (endless shelves, searchable with correct approach)
- The Prop Room (powerful items, some cursed)
- The Author's Desk (central mystery, guarded by The Critic)

**Primary Stat Affinity:** Script
**Secondary Stat Affinity:** Improv

### Archives Check Distribution

| Difficulty | Threshold | Percentage | Est. Count (25-35 nodes) |
|------------|-----------|------------|--------------------------|
| Basic | 1 | 20% | ~5-7 checks |
| Standard | 2 | 30% | ~8-10 checks |
| Advanced | 3 | 40% | ~10-14 checks |
| Expert | 4 | 10% | ~3-4 checks |

*Archives skews harder than Green Room due to investigation focus.*

### Investigation Mechanics

**Archive Searches:**
```
[ARCHIVE SEARCH: Script 2]
```
A specialized check for finding information in the Stacks. Functions like a stat check but may have multiple tiers of success.

| Result | Tier | Effect |
|--------|------|--------|
| Script 3+ | Deep Find | Complete information + bonus discovery |
| Script 2 | Standard Find | Information sought |
| Script 1 | Partial Find | Clue pointing to information |
| Script 0 | Lost | Time passes; minor complication |

**Discovery Chains:**
Some Archive nodes use connected discoveries:
```
[DISCOVERY CHAIN: 3 clues required]
- Clue A: Node 205 (Script 2)
- Clue B: Node 208 (Improv 2)
- Clue C: Node 211 (Stage Presence 2)
→ All three unlock Node 215 (The Truth)
```

### NPC Interactions: The Understudy

**Stat Affinity:** Script (research partner) / Stage Presence (emotional support)

| Node Range | Check | Type | Success | Failure |
|------------|-------|------|---------|---------|
| 200-202 | [STAT CHECK: Script 2] | Standard | Understudy shares research notes | Must find information independently |
| 205-207 | [STAT CHECK: Stage Presence 2] | Standard | Understudy opens up about identity crisis | Remains professionally distant |
| 210-212 | [STAT CHECK: Script 3] | Advanced | Together discover key revelation | Partial discovery; Understudy withholds |
| 215-218 | [COMBINED CHECK: Script 3 AND Stage Presence 2] | Combined | Understudy reveals Editor connection | Truth learned from other sources |

**Understudy Relationship Flags:**
- `UNDERSTUDY_PARTNER`: Research partnership established
- `UNDERSTUDY_CONFIDED`: They shared their origin fear
- `UNDERSTUDY_REVELATION`: Learned they may be connected to The Editor

### NPC Interactions: The Critic

**Stat Affinity:** Script (literary defense) / Stage Presence (confidence)

| Node Range | Check | Type | Success | Failure |
|------------|-------|------|---------|---------|
| 203-204 | [STAT CHECK: Stage Presence 2] | Standard | Stand ground against critique | Shaken; -1 to next check |
| 208-209 | [STAT CHECK: Script 3] | Advanced | Counter-critique effectively | Argument dismissed |
| 213-214 | [OPPOSED: Script vs. Critic's Judgment (4)] | Opposed | Prove your story's worth | Marked for "editing" |
| 220-222 | [STAT CHECK: Stage Presence 4] | Expert | Critic reveals vulnerability | Critic retreats, blocking path |

**The Critic is primarily an obstacle, not an ally. Defeating or evading The Critic is required to reach The Author's Desk.**

**Critic Encounter Flags:**
- `CRITIC_DEFEATED`: Won argument; Critic respects you
- `CRITIC_EVADED`: Avoided confrontation; Critic hunts you
- `CRITIC_WOUNDED`: Discovered Critic's grief; possible redemption path

### NPC Interactions: Lost Pages

**Stat Affinity:** Improv (chaotic communication) / Script (reconstruction)

| Node Range | Check | Type | Success | Failure |
|------------|-------|------|---------|---------|
| 206 | [STAT CHECK: Improv 2] | Standard | Communicate with Lost Pages | Gibberish only |
| 211 | [STAT CHECK: Script 2] | Standard | Reconstruct useful information | Fragments without context |
| 216 | [APPROACH CHECK: Improv 3 OR Script 3] | Combined | Lost Pages guide you safely | Navigate alone (harder) |

**Flags:** `PAGES_BEFRIENDED`, `PAGES_RESTORED` (helped a Lost Page become whole again)

---

## Act 2 Item Catalog

### Faction Tokens

| Item | Category | Source | Property | Effect |
|------|----------|--------|----------|--------|
| Director's Sigil | Token | Director relationship | — | Access to restricted Green Room areas |
| CHORUS Membership Card | Token | CHORUS induction | — | Collective memory access; minor hints |
| Preservationist Pin | Token | Faction alignment 5+ | — | +1 to checks with Preservationist NPCs |
| Revisionist Pen | Token | Faction alignment 5+ | Consumable | One-time rewrite of a minor narrative element |
| Exiter's Compass | Token | Faction alignment 5+ | — | Points toward the nearest exit from any story |
| Independent's Blank | Token | Independent path | — | Appears as whatever token is needed (one use per hub) |

### Archive Artifacts

| Item | Category | Source | Property | Effect |
|------|----------|--------|----------|--------|
| First Draft Fragment | Artifact | Archive search success | Plot-Critical | Reveals part of the Editor's plan |
| Author's Margin Notes | Script | Author's Desk (partial access) | — | Explains how the Understage was created |
| Prop of Power | Artifact | Prop Room (guarded) | Variable | Effect depends on which prop (sword, crown, key, etc.) |
| Understudy's Mirror | Artifact | Understudy gift | — | Reveals true nature of characters (once per hub) |
| Critic's Quill | Artifact | Critic defeat | Cursed | Powerful critique ability; may turn on user |
| Lost Page | Script | Lost Pages restored | Consumable | Fills in one gap in any knowledge check |

### Relationship-Gated Items

| Item | Requirement | Effect |
|------|-------------|--------|
| Director's Trust Seal | `DIRECTOR_CONFIDANT` | Opens private Director areas; reveals faction history |
| CHORUS Key | `CHORUS_MEMBER` | Access to CHORUS's hidden archives |
| The Final Girl's Warning | `FINAL_GIRL_TRUST` | One-time warning before a deadly trap |
| Solved Case's Casefile | `SOLVED_CASE_PARTNER` | +2 to one investigation check |
| Understudy's Research | `UNDERSTUDY_PARTNER` | Three clues toward the Revelation |

### Item Progression Notes

1. **Faction tokens** are mutually exclusive at high level (can only champion one faction)
2. **Archive artifacts** grow in power and danger as player approaches Author's Desk
3. **Relationship-gated items** reward consistent NPC investment
4. **Maximum items by end of Act 2:** 5-7 (within 5-item limit by requiring choices)

---

## Act 2 Flag System

### Story Progression Flags

| Flag | Trigger | Purpose |
|------|---------|---------|
| `ACT2_STARTED` | Enter Green Room | Marks Act 2 begin |
| `GREEN_ROOM_EXPLORED` | Visit all Green Room locations | Hub 2 complete flag |
| `ARCHIVES_DISCOVERED` | Find entrance to Archives | Hub 3 access |
| `ARCHIVES_EXPLORED` | Visit all Archive locations | Hub 3 complete flag |
| `REVELATION_UNLOCKED` | Gather 3+ clues about Editor | Act 2 climax available |
| `ACT2_COMPLETE` | Complete Revelation climax | Act 2 complete |

### Faction Alignment Flags

| Flag | Format | Example |
|------|--------|---------|
| Preservationist score | `PRESERVATIONIST: N` | `PRESERVATIONIST: 5` |
| Revisionist score | `REVISIONIST: N` | `REVISIONIST: 3` |
| Exiter score | `EXITER: N` | `EXITER: 7` |
| Independent eligibility | `INDEPENDENT_ELIGIBLE` | Set if all factions ≤3 |

### Relationship Flags: Hub 2 NPCs

| Flag | Trigger | Effect |
|------|---------|--------|
| `DIRECTOR_IMPRESSED` | First meeting success | Better social options |
| `DIRECTOR_SUSPICIOUS` | Challenged Director publicly | Watched more closely |
| `DIRECTOR_CONFIDANT` | Earned private audience | Revelation clues |
| `CHORUS_MEMBER` | Inducted into CHORUS | Collective memory access |
| `CHORUS_ALLY` | Helped CHORUS | They owe a favor |
| `CHORUS_DISMISSED` | Offended CHORUS | Information harder to get |
| `SOLVED_CASE_RESPECT` | Impressed with logic | Minor investigation help |
| `SOLVED_CASE_PARTNER` | Working together | Major investigation help |
| `QUEST_INSPIRED` | Encouraged action | May join Act 3 |
| `QUEST_ALLY` | Committed to helping | Joins Act 3 confrontation |
| `FINAL_GIRL_TRUST` | Earned respect | Survival advice; warnings |
| `HAPPY_ENDING_FRIEND` | Pleasant relationship | Revisionist philosophy access |
| `REVISIONIST_INSIDER` | Deep trust | Revision technique access |

### Relationship Flags: Hub 3 NPCs

| Flag | Trigger | Effect |
|------|---------|--------|
| `UNDERSTUDY_PARTNER` | Research partnership | Shared discoveries |
| `UNDERSTUDY_CONFIDED` | Emotional trust | Personal secrets |
| `UNDERSTUDY_REVELATION` | Full trust | Editor connection revealed |
| `CRITIC_DEFEATED` | Won argument | Critic respects you |
| `CRITIC_EVADED` | Avoided confrontation | Critic hunts you |
| `CRITIC_WOUNDED` | Found vulnerability | Redemption possible |
| `PAGES_BEFRIENDED` | Communicated successfully | Navigation help |
| `PAGES_RESTORED` | Helped a Page | Bonus item |

### Item Acquisition Flags

| Flag | Trigger | Effect |
|------|---------|--------|
| `HAS_DIRECTOR_SIGIL` | Director gift | Green Room access |
| `HAS_CHORUS_CARD` | CHORUS induction | Collective memory |
| `HAS_FACTION_TOKEN` | Faction champion | Faction bonus (varies) |
| `HAS_FIRST_DRAFT` | Archive discovery | Plot-critical; Revelation unlock |
| `HAS_UNDERSTUDY_MIRROR` | Understudy gift | Character insight |
| `HAS_CRITIC_QUILL` | Critic defeat | Dangerous power |

### Act 1 Carryover Flags

These Act 1 flags affect Act 2:

| Flag | Act 2 Effect |
|------|--------------|
| `CROSSING_DIRECT` | Director notices you; Stage Presence options +1 |
| `CROSSING_STEALTH` | CHORUS approaches first; Improv options +1 |
| `CROSSING_NEGOTIATED` | Guide introduces you; all factions start +1 |
| `CROSSING_DESPERATE` | Wildcard reputation; Improv checks -1 threshold |
| `MAREN_TRUST_HIGH` | Maren provides Green Room briefing |
| `MAREN_TRUST_LOW` | Must navigate Green Room alone |
| `PAWN_ALLIED` | Pawn provides intelligence on factions |
| `RUNAWAY_CAPTURED` | Director pleased; +1 Preservationist |
| `STAGEHAND_CURIOUS` | Stagehand appears in Archives with clues |

---

## Act 2 Climax: The Revelation

### Overview

The Revelation is the climax where the player discovers the truth about The Editor and the Final Draft. The approach and outcome depend on accumulated faction alignment and relationships.

**Prerequisites:**
- `REVELATION_UNLOCKED` flag set (3+ clues gathered)
- Access to Author's Desk (requires Critic resolution)

### Revelation Approaches

Based on dominant faction alignment:

| Faction | Approach | Revelation Truth Variant |
|---------|----------|--------------------------|
| **Preservationist** | Confront the conspiracy | Editor believes stagnation is killing stories; radical revision is salvation |
| **Revisionist** | Seek to understand and improve | Editor was once a Revisionist who went too far; wants to undo their own edits |
| **Exiter** | Free the trapped truth | Editor wants to destroy the boundary entirely; freedom through annihilation |
| **Independent** | Observe without faction lens | Editor is responding to external threat; writing a story to save stories |

### Revelation Mechanics

**Entry Checks:**

| Approach | Check | Type | Success | Failure |
|----------|-------|------|---------|---------|
| Preservationist | [STAT CHECK: Script 3] | Advanced | Full truth revealed | Partial truth; must fill gaps |
| Revisionist | [STAT CHECK: Stage Presence 3] | Advanced | Editor's perspective understood | Simplified version only |
| Exiter | [STAT CHECK: Improv 3] | Advanced | Freedom implications clear | Consequences unclear |
| Independent | [COMBINED CHECK: Script 2 AND Stage Presence 2 AND Improv 2] | Special | All perspectives visible | Single perspective based on highest stat |

### Act 3 Opening Conditions

Based on Revelation outcome:

| Revelation Result | Act 3 Opening |
|-------------------|---------------|
| **Full Truth + Faction Champion** | Faction rallies behind you; start with allies |
| **Full Truth + Independent** | All factions wary; must earn trust individually |
| **Partial Truth** | Must investigate further in Act 3; delayed start |
| **Allies Present** | NPCs with ALLY flags join you for Act 3 |
| **Understudy Revelation** | Understudy's Editor connection creates complication |
| **Critic Defeated** | Archives accessible in Act 3 for research |
| **Critic Evaded** | Critic pursues into Act 3 as secondary antagonist |

### Climax Flags

| Flag | Trigger | Effect |
|------|---------|--------|
| `REVELATION_PRESERVATIONIST` | Dominant faction | Preservationist Act 3 truth |
| `REVELATION_REVISIONIST` | Dominant faction | Revisionist Act 3 truth |
| `REVELATION_EXITER` | Dominant faction | Exiter Act 3 truth |
| `REVELATION_INDEPENDENT` | No dominant faction | Independent Act 3 truth |
| `REVELATION_COMPLETE` | Full truth accessed | Strongest Act 3 position |
| `REVELATION_PARTIAL` | Partial truth only | Must investigate in Act 3 |

---

## Balance Verification Checklist

Before Act 2 nodes are written, verify against these constraints:

### Difficulty Curve Compliance

- [ ] Hub 2: 50% Basic/Standard, 40% Advanced, 10% Expert
- [ ] Hub 3: 50% Basic/Standard, 40% Advanced, 10% Expert (skewing slightly harder)
- [ ] No more than 4 Expert (threshold 4) checks total
- [ ] Expert checks always have alternative paths

### Fail-Forward Verification

- [ ] Every check has explicit success AND failure paths
- [ ] No failure leads to game-over
- [ ] Failure paths provide different content, not less content
- [ ] The Critic cannot permanently block progress

### Faction Parity

- [ ] Each faction has roughly equal content (8-12 nodes each)
- [ ] Each faction has 2-3 unique relationship opportunities
- [ ] Independent path is harder but viable (15-20% of players estimated)
- [ ] No faction is portrayed as "correct" or "evil"

### NPC Relationship Balance

- [ ] Each Hub 2 NPC has 3-5 interaction nodes
- [ ] Each Hub 3 NPC has 3-5 interaction nodes
- [ ] Relationship flags unlock meaningful rewards, not required content
- [ ] No relationship is required for Act 2 completion

### Item Balance

- [ ] Faction tokens require commitment (alignment 5+)
- [ ] Archive artifacts increase in power and risk toward the end
- [ ] No item is required for Act 2 completion
- [ ] Player can end Act 2 with 4-6 items (manageable inventory)

### Flag Consistency

- [ ] All flags use UPPERCASE_SNAKE_CASE
- [ ] Faction flags use NAME: N format
- [ ] Relationship flags use NPC_RELATIONSHIP_LEVEL format
- [ ] Carryover from Act 1 is clearly documented

---

## Implementation Notes

### For Node Authors

1. **Reference this document** before writing any Act 2 node
2. **Track faction implications** for every meaningful choice
3. **Use exact check format**: `[STAT CHECK: Stat N]` or `[ARCHIVE SEARCH: Script N]`
4. **Include both paths**: Every check needs success AND failure text
5. **Update catalogs**: Add new items/flags to this document when created
6. **Cross-reference relationships**: NPCs should reference each other appropriately

### Cross-Document References

- **RULES.md**: Core mechanics, stat definitions, check format
- **OUTLINE.md**: Story structure, hub descriptions, climax requirements
- **STYLE.md**: Node formatting, prose conventions
- **CHARACTERS.md**: NPC details, voice notes, relationship maps
- **ACT1_MECHANICS.md**: Carryover flags, established patterns

### Open Questions for Act 3 Mechanics

1. How do faction champions interact with the Editor confrontation?
2. Should Independent path allow faction alliance in Act 3, or remain truly solo?
3. Does The Critic redemption path affect the ending?
4. How does Understudy's Editor connection resolve?

---

*This document specifies Act 2 mechanics. It should be updated as nodes are written and playtested.*

---
