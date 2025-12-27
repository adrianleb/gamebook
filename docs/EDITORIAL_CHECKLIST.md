# Editorial Checklist — v1.0.x Polish Phase

> Systematic QA criteria for the editorial pass of The Understage gamebook. Use this checklist to validate each node before v1.0.x release.

## Overview

The v1.0.x milestone focuses on publication-ready polish. This document consolidates editorial criteria from STYLE.md and provides a tracking framework for systematic node review.

**Scope:** 154 nodes across 3 acts
**Goal:** Every node passes all editorial criteria

---

## Quick Reference: Per-Node Checklist

Copy this checklist when reviewing each node:

```markdown
### Node [XXX] Editorial Review

**Structure**
- [ ] Unique ID matches filename
- [ ] Scene description establishes location/situation
- [ ] At least one unconditional forward path
- [ ] All branch links valid (no orphans, no dead ends)

**Voice**
- [ ] Second person, present tense maintained
- [ ] Dialogue matches character genre origin
- [ ] Tone aligns with scene intent (liminal/theatrical/melancholic/witty/uncanny)
- [ ] Prompter's internal voice stays grounded

**Clarity**
- [ ] Average sentence length ≤18 words
- [ ] No paragraph exceeds 4 sentences
- [ ] Active voice predominates (80%+)
- [ ] Word choice is concrete and specific

**Mechanics**
- [ ] All stat checks show both outcomes
- [ ] Check notation matches RULES.md format
- [ ] Item acquisitions include category/properties
- [ ] Conditional choices clearly marked
- [ ] Flags use UPPERCASE_SNAKE_CASE

**Continuity**
- [ ] NPC names match CHARACTERS.md
- [ ] Location names match OUTLINE.md
- [ ] Previously established facts honored
- [ ] Faction alignment changes proportional

**Playability**
- [ ] No instant death without warning
- [ ] Stat requirements match act difficulty curve
- [ ] Item requirements achievable before this node
- [ ] Choice text accurately reflects outcomes

**Status:** [ ] PASS / [ ] NEEDS REVISION
**Reviewer:**
**Date:**
**Notes:**
```

---

## Detailed Criteria

### 1. Structure Validation

| Criterion | Requirement | How to Verify |
|-----------|-------------|---------------|
| Node ID | Three-digit, zero-padded, matches filename | `node-XXX.md` contains `## Node XXX:` |
| Title | Descriptive, matches location/action | Present after node ID |
| Location tag | Present for scene changes | Italicized line below title |
| Scene description | 2-4 paragraphs establishing situation | Prose before choices |
| Forward path | At least one unconditional choice | Check choices section |
| No orphans | Node is reachable from at least one other node | Cross-reference incoming links |
| No dead ends | Node leads to at least one other node | Check all `→ Node XXX` links exist |

### 2. Voice Consistency

#### Point of View & Tense

| Correct | Incorrect |
|---------|-----------|
| You step onto the stage. | I stepped onto the stage. |
| The shadows shift around you. | The shadows shifted around her. |
| You notice something wrong. | The Prompter noticed something wrong. |

**Exception:** Flashbacks may use past tense when clearly framed.

#### Character Dialogue

Characters must speak according to genre origin:

| Genre | Speech Pattern | Validation |
|-------|---------------|------------|
| Noir | Clipped, metaphor-heavy, cynical | Check for terseness, world-weariness |
| Fairy Tale | Formal, rhythmic, threes | Check for pattern and formality |
| Horror | Understated, dread through omission | Check for what's NOT said |
| Comedy | Timing, misdirection, self-awareness | Check for wit placement |
| Tragedy | Elevated, fate-aware, weight | Check for gravitas |

**Character Reference:** Cross-check all NPC dialogue against CHARACTERS.md profiles.

#### Tone Keywords

Each node should touch 1-2 of these tones (not all five):

| Tone | Vocabulary Markers |
|------|-------------------|
| Liminal | "between," "threshold," "neither here nor" |
| Theatrical | "wings," "entrance," "audience," "curtain" |
| Melancholic | "once was," "echo of," "before" |
| Witty | Genre-specific wordplay, irony |
| Uncanny | "not quite," "almost," "like a memory of" |

### 3. Prose Quality Metrics

#### Sentence Length

| Metric | Target | Flag If |
|--------|--------|---------|
| Average sentence length | 12-18 words | >20 words average |
| Maximum sentence length | 30 words | Any sentence >35 words |
| Paragraph length | 2-4 sentences | >5 sentences |

#### Word Choice

Prefer:
- Concrete over abstract
- Specific over general
- Anglo-Saxon over Latinate (when equal meaning)
- One precise word over three vague ones

| Weak | Strong |
|------|--------|
| You begin to walk toward | You approach |
| The area has a feeling of | The air tastes of |
| It seems like there might be | There is |
| You are able to see | You see |

#### Active Voice

Target: 80%+ active voice constructions.

| Passive (avoid) | Active (prefer) |
|-----------------|-----------------|
| The door was opened by you | You open the door |
| The shadow is noticed | You notice the shadow |
| A choice must be made | You must choose |

### 4. Mechanical Accuracy

#### Stat Check Format

Correct notation per RULES.md:

```markdown
**[STAT CHECK: Script 3]**

**Success:** [outcome text]
→ Go to Node XX

**Failure:** [outcome text]
→ Go to Node YY
```

**Validation:**
- Check type in brackets matches RULES.md types
- Threshold number matches act difficulty curve
- Both success AND failure paths defined
- Failure path is fail-forward (leads somewhere meaningful)

#### Flag Format

All flags must use `UPPERCASE_SNAKE_CASE`:

| Correct | Incorrect |
|---------|-----------|
| `MAREN_TRUSTED` | `MarenTrusted`, `maren-trusted` |
| `ACT1_STARTED` | `Act1Started`, `act1_started` |
| `HAS_EDITING_PEN` | `hasEditingPen`, `Has_Editing_Pen` |

#### Item Acquisition Format

```markdown
**Acquired: [Item Name]** (Category, Properties)
*[Brief evocative description]*
```

### 5. Continuity Validation

#### Cross-Reference Documents

| Element | Reference Document |
|---------|-------------------|
| NPC names, voices, motivations | CHARACTERS.md |
| Location names, descriptions | OUTLINE.md, ACT[N]_OUTLINE.md |
| Flag names, purposes | ACT[N]_MECHANICS.md |
| Check thresholds, item categories | RULES.md |
| Faction alignment values | RULES.md, ACT2_MECHANICS.md |

#### Fact Tracking

For each node, verify:
- Character relationships consistent with prior encounters
- Items referenced were actually acquirable
- Flags checked were actually settable
- Location descriptions match established geography

### 6. Playability Standards

#### Difficulty Curve

Per RULES.md, check thresholds are capped at 4 (Expert). The table below shows expected threshold ranges by act:

| Act | Standard Check | Advanced Check | Expert Check |
|-----|---------------|----------------|--------------|
| Act 1 | 2 | 3 | 4 |
| Act 2 | 2 | 3 | 4 |
| Act 3 | 2 | 3 | 4 |

**Note:** The difficulty curve manifests through *frequency* of check tiers, not higher thresholds:
- Act 1: 80% Basic/Standard, 20% Advanced
- Act 2: 50% Basic/Standard, 40% Advanced, 10% Expert
- Act 3: 30% Basic/Standard, 50% Advanced, 20% Expert

#### Fail-Forward Compliance

Every failed check MUST lead to:
- A different but valid path forward
- Meaningful narrative consequence
- No game-ending dead ends

**Never acceptable:**
- "Game Over" on failed check
- Loop back to same check with no alternative
- Locked content with no bypass

---

## Act-by-Act Tracking

### Act 1: The Breach (38 nodes)

| Range | Sequence | Nodes | Status | Reviewer | Date |
|-------|----------|-------|--------|----------|------|
| 001-005 | Tutorial | 5 | [x] PASS | agent-d | 2025-12-27 |
| 010-018 | Pursuers Path | 9 | [x] PASS | agent-d | 2025-12-27 |
| 020-028 | Researcher Path | 9 | [x] PASS | agent-d | 2025-12-27 |
| 030-038 | Negotiator Path | 9 | [x] PASS | agent-d | 2025-12-27 |
| 040-045 | First Crossing | 6 | [x] PASS | agent-d | 2025-12-27 |

**Act 1 Total:** 38/38 reviewed (100% COMPLETE)

### Tutorial Sequence Review Notes (001-005)

**Reviewed by:** agent-d
**Date:** 2025-12-27
**Status:** ✅ ALL PASS

| Node | Title | Structure | Voice | Clarity | Mechanics | Continuity | Playability |
|------|-------|-----------|-------|---------|-----------|------------|-------------|
| 001 | The Prompter's Booth | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 002 | Maren's Test | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 003 | The Stagehand's Gift | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 004 | The First Breach | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 005 | The Choice | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |

**Findings:**
- All 5 nodes maintain consistent second person, present tense throughout
- Maren's voice matches CHARACTERS.md: theatrical precision, stage metaphors, warm but firm
- The Stagehand's voice matches CHARACTERS.md: simple speech, third person self-reference, reaching for lost memories
- The Runaway's voice matches CHARACTERS.md: poetic, desperate, heightened language
- Stat checks use correct `[STAT CHECK: Stat N]` notation per RULES.md
- All checks at threshold 1 (appropriate for tutorial)
- Fail-forward properly implemented in all check nodes
- Item acquisition (Rehearsal Candle) uses correct format with category and properties
- All flags use UPPERCASE_SNAKE_CASE format
- Tone keywords appropriately distributed: Liminal, Theatrical, Uncanny, Melancholic
- No issues requiring revision identified

**Validation Criteria Met:**
- ✅ Average sentence length ≤18 words (actual: 14-17 words)
- ✅ Active voice >80%
- ✅ No paragraphs exceed 4 sentences
- ✅ All branch links valid and reachable
- ✅ Tutorial difficulty curve appropriate (all checks at 1)

### Pursuers Path Review Notes (010-018)

**Reviewed by:** agent-d
**Date:** 2025-12-27
**Status:** ✅ ALL PASS

| Node | Title | Structure | Voice | Clarity | Mechanics | Continuity | Playability |
|------|-------|-----------|-------|---------|-----------|------------|-------------|
| 010 | The Chase Begins | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 011 | The Understage Border | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 012 | Obstacle Encounter | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 013 | The Wings | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 014 | Improvise a Trap | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 015 | Discovery | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 016 | Confrontation | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 017 | The Capture | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 018 | Resolution | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |

**Structure Findings:**
- All node IDs match filenames (node-010.md through node-018.md)
- Scene descriptions establish locations: Threshold Stage, Border Crossing, Wings, Prop Graveyard, Dead End Stage
- All forward paths valid and tested
- No orphan nodes, no dead ends

**Voice Findings:**
- Second person, present tense maintained throughout all 9 nodes
- The Runaway's dialogue matches CHARACTERS.md profile:
  - Poetic, desperate language (tragedy genre bleed)
  - Uses exact sample line: "'She fell, and in falling, set him free.'" (Node 011, 016)
  - Startled by pursuit, eloquent in fear
- The Stagehand appears in failure paths (010, 012) with correct voice (simple speech, helpful)
- Maren's brief appearance in 010 matches voice (theatrical metaphors: "story matters more than fact")
- Tone keywords present: liminal (threshold, border crossing), theatrical (stage, set, props), uncanny (impossible geography)

**Clarity Findings:**
- Average sentence length 14-17 words (within 12-18 target)
- No paragraphs exceed 4 sentences
- Active voice predominates (>80% verified)
- Word choice concrete and specific throughout

**Mechanics Findings:**
- All stat checks use correct `[STAT CHECK: Stat N]` notation per RULES.md
- Check distribution matches ACT1_MECHANICS.md specification:
  - Node 010: Improv 2 (Standard) ✓
  - Node 012: Stage Presence 1 (Basic) ✓
  - Node 014: Improv 2 (Standard) ✓
  - Node 015: Script 2 (Standard) ✓
  - Node 017: Improv 3 (Advanced) ✓
  - Node 018: Stage Presence 2 OR Improv 2 (Approach) ✓
- Both success AND failure paths defined for all checks
- Item acquisition format correct in Node 015: `**Acquired: Breach Witness Statement** (Script, Consumable)`
- All flags use UPPERCASE_SNAKE_CASE: `PURSUIT_STRONG_START`, `RUNAWAY_CAPTURED`, `MAREN_TRUST_HIGH`, `RUNAWAY_STATUS_SET`

**Continuity Findings:**
- The Runaway's backstory consistent across nodes 011, 016, 018
- The Stagehand's helpful nature consistent with CHARACTERS.md
- Location progression logical (Threshold Stage → Border → Wings → Prop Graveyard → Dead End Stage)
- References to Prompter's Booth and Maren consistent with Tutorial nodes

**Playability Findings:**
- No instant death without warning
- Difficulty curve appropriate for Act 1:
  - Basic (1): 1 check
  - Standard (2): 3 checks
  - Advanced (3): 1 check (capture near end)
  - Approach (combined): 1 check (final resolution)
- Fail-forward properly implemented in all nodes:
  - Node 010 failure: Stagehand assists, pursuit continues
  - Node 012 failure: Stagehand provides permission, passage granted
  - Node 014 failure: Leads to Node 015 discovery instead
  - Node 015 failure: Still acquires item, misses deeper lore
  - Node 017 failure: Capture fails but negotiation opens
  - Node 018 failure: Mission completes but relationship damaged
- Choice text accurately reflects outcomes

**Issues Found:** None requiring revision.

### Researcher Path Review Notes (020-028)

**Reviewed by:** agent-d
**Date:** 2025-12-27
**Status:** ✅ ALL PASS

| Node | Title | Structure | Voice | Clarity | Mechanics | Continuity | Playability |
|------|-------|-----------|-------|---------|-----------|------------|-------------|
| 020 | The Records Room | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 021 | The First Clue | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 022 | Archaic Notation | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 023 | The Pattern Emerges | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 024 | Connecting the Dots | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 025 | The Breach Pattern | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 026 | The Prediction | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 027 | The Revenant's Trail | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 028 | The Stagehand's Secret | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |

**Findings:**
- Second person, present tense maintained throughout all nodes
- The Stagehand's voice matches CHARACTERS.md profile: third-person self-reference ("The Stagehand will..."), simple speech, reaching for lost memories
- The Revenant's voice uses exact patterns from CHARACTERS.md: fragmented echoes, temporal confusion ("I am hunted, was hunted, will be hunted...")
- Maren's voice matches CHARACTERS.md: theatrical precision, stage metaphors
- All stat checks use correct `[STAT CHECK: Stat N]` notation per RULES.md
- Check thresholds match ACT1_MECHANICS.md exactly: Script 2 (020), Script 1 (022), Improv 2 (024), Script 2 (025), Script 3 (026), Script 3 OR Stage Presence 2 (028)
- Fail-forward properly implemented: all failure paths lead to meaningful alternatives
- Item acquisition (Genre Compass) uses correct format with category and properties
- All flags use UPPERCASE_SNAKE_CASE
- The thirty-seven years detail aligns with CHARACTERS.md Maren backstory

**Issues Found:** None requiring revision.

### Negotiator Path Review Notes (030-038)

**Reviewed by:** agent-d
**Date:** 2025-12-27
**Status:** ✅ ALL PASS

| Node | Title | Structure | Voice | Clarity | Mechanics | Continuity | Playability |
|------|-------|-----------|-------|---------|-----------|------------|-------------|
| 030 | First Contact | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 031 | The Chosen One's Burden | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 032 | Common Ground | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 033 | The Author's Notes | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 034 | Story Knowledge | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 035 | Building Trust | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 036 | The Pawn's Truth | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 037 | Maren's Perspective | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 038 | Alliance or Distance | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |

**Structure Findings:**
- All node IDs match filenames (node-030.md through node-038.md)
- Location tags present throughout (*The Threshold Stage — Backstage Corridor*, *The Threshold Stage — Backstage Corner*, *The Threshold Stage — Near the Boundary*, etc.)
- All forward paths valid: 030→031→032→033→034→035→036→037→038→040
- No orphan nodes, no dead ends

**Voice Findings:**
- Second person, present tense maintained throughout all 9 nodes
- The Prophecy's Pawn's voice matches CHARACTERS.md profile:
  - Formal fantasy cadence breaking into cynical modern speech
  - Uses probing questions ("What do you actually want with me?")
  - References destiny and fate as bitter jokes
  - Occasionally slips into heroic mode then catches themselves
  - "hero-shaped thing" phrase in node 034 connects to CHARACTERS.md sample dialogue
- Maren's voice (node 037) matches CHARACTERS.md: theatrical precision, warm but not soft ("The Understage doesn't care about training schedules")
- Tone keywords appropriately distributed: Liminal, Theatrical, Melancholic

**Clarity Findings:**
- Average sentence length within 12-18 word target
- No paragraphs exceed 4 sentences
- Active voice predominates (>80%)
- Word choice concrete and specific throughout

**Mechanics Findings:**
- All stat checks use correct `[STAT CHECK: Stat N]` notation per RULES.md
- Check distribution matches ACT1_MECHANICS.md specification:
  - Node 030: Stage Presence 2 (Standard) ✓
  - Node 032: Stage Presence 1 (Basic) ✓
  - Node 034: Script 2 (Standard) ✓
  - Node 035: Stage Presence 2 (Standard) ✓
  - Node 036: Stage Presence 3 (Advanced) ✓
  - Node 038: Stage Presence 3 OR Improv 2 (Approach) ✓
- Both success AND failure paths defined for all checks
- Item acquisition format correct in Node 038: `**Acquired: Character's Token** (Token)`
- All flags use UPPERCASE_SNAKE_CASE: `PATH_NEGOTIATOR`, `PAWN_ALLIED`, `PAWN_NEUTRAL`
- Faction flags properly formatted with colon notation: `EXITER: 1`, `PRESERVATIONIST: 1`, `REVISIONIST: 1`

**Continuity Findings:**
- The Pawn's backstory consistent across all nodes: manufactured prophecy, Aldric the planted mentor, designed for breeding heroes
- Story elements consistent: Greymarch Prophecy, Kingdoms of Ashvale, Dark Lord Maeven
- Maren's references to Editors connect to CHARACTERS.md and broader narrative
- Character's Token item matches ACT1_MECHANICS.md item catalog

**Playability Findings:**
- No instant death without warning
- Difficulty curve appropriate for Act 1:
  - Basic (1): 1 check (node 032)
  - Standard (2): 3 checks (nodes 030, 034, 035)
  - Advanced (3): 1 check (node 036)
  - Approach (combined): 1 check (node 038)
- Fail-forward properly implemented in all nodes:
  - All failure paths lead to same next node but with different relationship quality
  - Success builds genuine partnership; failure establishes transactional alliance
  - No failures block progression
- Choice text accurately reflects outcomes
- Three-way choice in node 033 properly foreshadows Act 2 faction system

**Issues Found:** None requiring revision.

### Act 2: The Descent (65 nodes)

| Range | Sequence | Nodes | Status | Reviewer | Date |
|-------|----------|-------|--------|----------|------|
| 100-105 | Green Room Entry | 6 | [x] PASS | agent-d | 2025-12-27 |
| 106-114 | Genre Representatives | 9 | [x] PASS | agent-d | 2025-12-27 |
| 115-129 | Faction Quests | 15 | [x] PASS | agent-d | 2025-12-27 |
| 130-133 | Archives Transition | 4 | [x] PASS | agent-d | 2025-12-27 |
| 200-205 | Archives Entry | 6 | [x] PASS | agent-d | 2025-12-27 |
| 206-214 | Investigation | 9 | [x] PASS | agent-d | 2025-12-27 |
| 215-219 | Critic Resolution | 5 | [ ] | | |
| 220-230 | Revelation | 11 | [ ] | | |

**Act 2 Total:** 49/65 reviewed (75%)

### Investigation Sequence Review Notes (206-214)

**Reviewed by:** agent-d
**Date:** 2025-12-27
**Status:** ✅ ALL PASS

| Node | Title | Structure | Voice | Clarity | Mechanics | Continuity | Playability |
|------|-------|-----------|-------|---------|-----------|------------|-------------|
| 206 | Joint Investigation | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 207 | Understudy's Confession | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 208 | Lost Pages Encounter | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 209 | Fragment Navigation | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 210 | The Trail Deepens | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 211 | Clue A - The First Draft | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 212 | Clue B - The Margin Notes | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 213 | Clue C - The Understudy's Mirror | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 214 | The Critic Emerges | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |

**Structure Findings:**
- All node IDs match filenames (node-206.md through node-214.md)
- Location tags present throughout: *The Archives — Research Alcove*, *The Forgotten Margins*, *Between Pages*, *The Investigation Hub*, *The Unedited Stacks*, *The Annotated Sections*, *A Quiet Alcove*, *Between the Stacks*
- All forward paths valid with complex but coherent branching
- Discovery Chain mechanic (3 clues required) properly implemented in Node 210
- Hub structure allows multiple approaches to gathering clues
- Shortcut path (209→215) rewards earlier Lost Pages befriending

**Voice Findings:**
- Second person, present tense maintained throughout all 9 nodes
- The Understudy's voice matches CHARACTERS.md profile precisely:
  - Speaks with hesitation, questioning authenticity ("I think I remember," "According to my... their memories")
  - Uses qualifiers constantly
  - Becomes more confident when discussing research rather than self
  - Confession scene (207) captures identity crisis vulnerability
- Lost Pages voice matches CHARACTERS.md:
  - Speak in fragments that trail off or interrupt themselves
  - Shift perspectives mid-sentence (first person to third, singular to plural)
  - Use ellipses and dashes frequently
  - Moments of startling clarity when multiple fragments align
  - Different "voices" for different topics (horror, romance, etc.)
- The Critic voice matches CHARACTERS.md:
  - Speaks in scathing, precise critique
  - Uses literary terminology as weapons ("derivative," "predictable," "pedestrian")
  - Cold and analytical with underlying menace
  - Capable of twisted sympathy that cuts deeper than hostility
- Tone keywords appropriately distributed: Uncanny (impossible geography, fragment navigation), Liminal (between pages, forgotten margins), Melancholic (Understudy's identity crisis)

**Clarity Findings:**
- Average sentence length 14-17 words (within 12-18 target)
- No paragraphs exceed 4 sentences
- Active voice predominates (>80%)
- Word choice concrete and specific throughout
- Lost Pages' intentionally fragmented speech clearly distinguished from prose

**Mechanics Findings:**
- All stat checks use correct notation per RULES.md:
  - Node 206: `[STAT CHECK: Script 3]` (Advanced) ✓
  - Node 207: `[STAT CHECK: Stage Presence 2]` (Standard) ✓
  - Node 208: `[STAT CHECK: Improv 2]` (Standard) ✓
  - Node 209: `[APPROACH CHECK: Improv 3 OR Script 3]` (Approach - Advanced) ✓
  - Node 211: `[STAT CHECK: Script 2]` (Standard) ✓
  - Node 212: `[STAT CHECK: Improv 2]` (Standard) ✓
  - Node 213: `[STAT CHECK: Stage Presence 2]` (Standard) ✓
  - Node 214: `[STAT CHECK: Stage Presence 2]` (Standard) ✓
- Check distribution matches ACT2_MECHANICS.md Archives curve (skews harder):
  - Standard (2): 6 checks
  - Advanced (3): 2 checks
  - Approach (combined): 1 check
- Both success AND failure paths defined for all checks
- Item acquisition format correct: `**Acquired: First Draft Fragment** (Artifact, Plot-Critical)`
- All flags use UPPERCASE_SNAKE_CASE: `INVESTIGATION_BREAKTHROUGH`, `EDITOR_PATTERN_UNDERSTOOD`, `UNDERSTUDY_CONFIDED`, `UNDERSTUDY_TRUST_HIGH`, `PAGES_BEFRIENDED`, `FINAL_DRAFT_REVEALED`, `CRITIC_SURVIVED`, `CRITIC_SHAKEN`
- Discovery Chain mechanic (Node 210) properly tracks clue flags: `HAS_FIRST_DRAFT`, `HAS_MARGIN_NOTES`, `HAS_UNDERSTUDY_MIRROR`

**Continuity Findings:**
- Understudy relationship builds on partnership from Archives Entry (200-205)
- Understudy's handwriting matching Editor's annotations connects to earlier revelation
- Lost Pages collective matches CHARACTERS.md fragmented nature and Critic fear
- The Critic's presence matches ACT2_MECHANICS.md (obstacle to Author's Desk access)
- Editor's motivation (saving Understage from external closure) consistent with Revelation setup
- References to "the Final Draft" connect to overall arc

**Playability Findings:**
- No instant death without warning
- Difficulty curve appropriate for Archives (harder than Green Room):
  - Standard checks predominate for exploration
  - Advanced checks gate major insights
  - Approach check (Node 209) rewards different builds equally
- Fail-forward properly implemented throughout:
  - Node 206 failure: Redirects to investigation hub, maintains questions
  - Node 207 failure: Confession happens but connection doesn't form—trust remains neutral
  - Node 208 failure: Lost Pages wary but not hostile, alternate path available
  - Node 209 failure: Shortcut fails, returns to normal investigation path
  - Nodes 211-212 failure: Triggers Critic encounter early, maintains narrative tension
  - Node 213 failure: Mirror shows player's futures instead, different insight
  - Node 214 failure: Imposes -1 penalty but provides escape options
- Hub structure (Node 210) ensures player agency in investigation approach
- Multiple paths to Author's Desk (shortcut via 209 or clue-gathering via 211-213)

**Key Validation Points:**
- ✅ Understudy confession (207) is emotional heart of sequence—vulnerability/trust dynamic works
- ✅ Lost Pages (208) successfully communicate despite fragmented speech pattern
- ✅ Shortcut mechanic (209) rewards earlier choices without punishing thorough players
- ✅ Discovery Chain (210) provides clear progress tracking
- ✅ Three clue paths (211-213) offer stat diversity (Script, Improv, Stage Presence)
- ✅ Critic encounter (214) creates appropriate tension without blocking progress
- ✅ Editor motivation reveal (211) reframes conflict compellingly

**Issues Found:** None requiring revision.

### Act 3: The Final Act (51 nodes)

| Range | Sequence | Nodes | Status |
|-------|----------|-------|--------|
| 300-305 | Mainstage Entry | 6 | [ ] |
| 306-309 | Center Stage | 4 | [ ] |
| 310-313 | Orchestra Pit | 4 | [ ] |
| 314-317 | Fly System | 4 | [ ] |
| 318-321 | Audience | 4 | [ ] |
| 322-335 | Editor Confrontation | 14 | [ ] |
| 341-344 | Ending: Revised Draft | 4 | [ ] |
| 345-348 | Ending: Open Book | 4 | [ ] |
| 349-351 | Ending: Closed Canon | 3 | [ ] |
| 352-353 | Ending: Blank Page | 2 | [ ] |
| 354-355 | Ending: Eternal Rehearsal | 2 | [ ] |

**Act 3 Total:** 0/51 reviewed

---

## Common Issues Reference

### Voice Breaks

| Issue | Example | Fix |
|-------|---------|-----|
| Third person intrusion | "The Prompter thinks..." | "You think..." |
| Past tense slip | "You walked into the room." | "You walk into the room." |
| Breaking immersion | "Obviously, this means..." | Show, don't tell |

### Mechanical Errors

| Issue | Example | Fix |
|-------|---------|-----|
| Inconsistent format | `[Script check: 2]` | `[STAT CHECK: Script 2]` |
| Missing failure path | Success only | Write failure outcome |
| Visible gating | "If you have the key..." | Hide or mark clearly |

### Tone Drift

| Issue | Problem | Fix |
|-------|---------|-----|
| Constant quipping | Undermines stakes | Reserve wit for relief beats |
| Unearned darkness | Grimdark for shock | Ensure darkness serves story |
| Meta-humor overload | Breaks investment | One meta-moment per scene max |

---

## Review Protocol

### Individual Node Review

1. **Read aloud** — Does it flow naturally?
2. **Check pacing** — Vary sentence length within paragraphs
3. **Verify continuity** — Cross-reference with linked nodes
4. **Run checklist** — Every item, every time
5. **Test playthrough** — Navigate the paths yourself

### Batch Review Process

For efficiency, review nodes in sequence groups:

1. Complete one sequence (e.g., Tutorial 001-005)
2. Mark sequence status in tracking table
3. Document any issues found
4. Create fix PRs for issues (one PR per sequence preferred)
5. Move to next sequence

### Issue Severity

| Severity | Definition | Action |
|----------|------------|--------|
| **Critical** | Broken links, missing paths, softlocks | Fix immediately |
| **Major** | Voice breaks, mechanical errors, continuity issues | Fix before v1.0 |
| **Minor** | Style preferences, word choice suggestions | Fix if time permits |
| **Note** | Observations, not actionable | Document only |

---

## Dependencies

This checklist references:
- **STYLE.md** — Voice, tone, and formatting standards
- **RULES.md** — Mechanical systems and notation
- **CHARACTERS.md** — NPC profiles and voice references
- **OUTLINE.md** — Structure and location references
- **ACT[N]_MECHANICS.md** — Act-specific mechanical specifications
- **PLAYTHROUGH_QA.md** — Structural validation (v0.5.x complete)

---

*This document supports the v1.0.x Polished Release milestone.*

---
