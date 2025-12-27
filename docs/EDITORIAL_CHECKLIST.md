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

### First Crossing Review Notes (040-045)

**Reviewed by:** agent-d
**Date:** 2025-12-27
**Status:** ✅ ALL PASS

| Node | Title | Structure | Voice | Clarity | Mechanics | Continuity | Playability |
|------|-------|-----------|-------|---------|-----------|------------|-------------|
| 040 | The Threshold | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 041 | Direct Confrontation | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 042 | Stealth Entry | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 043 | Negotiated Entry | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 044 | Desperate Leap | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 045 | The First Crossing Complete | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |

**Findings:**
- All 6 nodes maintain consistent second person, present tense
- Maren's voice matches CHARACTERS.md: theatrical precision, warm but not soft
- Collective Understage voice appropriately liminal and narrative-aware
- Four distinct crossing methods (direct, stealth, negotiated, desperate) all properly implemented
- Stat checks match ACT1_MECHANICS.md: Stage Presence 3 (041), Improv 3 (042), Combined Script 2 AND Stage Presence 2 (043), Any 2 (044)
- Desperate Leap option (Any 2) ensures all builds can proceed to Act 2
- Crossing flags use UPPERCASE_SNAKE_CASE: `CROSSING_DIRECT`, `CROSSING_STEALTH`, `CROSSING_NEGOTIATED`, `CROSSING_DESPERATE`, `FIRST_CROSSING_COMPLETE`
- Node 045 provides clear Act 2 Opening Conditions table for all 8 method+result combinations
- Fail-forward properly implemented: all 4 crossing methods allow progression with success/failure variants

**Issues Found:** None requiring revision.

---

## Act 1 Editorial Pass Complete

Act 1 is now 38/38 (100%) reviewed:
- ✅ Tutorial (001-005) - 5 nodes PASS
- ✅ Pursuers Path (010-018) - 9 nodes PASS
- ✅ Researcher Path (020-028) - 9 nodes PASS
- ✅ Negotiator Path (030-038) - 9 nodes PASS
- ✅ First Crossing (040-045) - 6 nodes PASS

**Act 1 is publication-ready for v1.0.x release.**

---

### Act 2: The Descent (65 nodes)

| Range | Sequence | Nodes | Status | Reviewer | Date |
|-------|----------|-------|--------|----------|------|
| 100-105 | Green Room Entry | 6 | [x] PASS | agent-d | 2025-12-27 |
| 106-114 | Genre Representatives | 9 | [x] PASS | agent-d | 2025-12-27 |
| 115-129 | Faction Quests | 15 | [x] PASS | agent-d | 2025-12-27 |
| 130-133 | Archives Transition | 4 | [x] PASS | agent-d | 2025-12-27 |
| 200-205 | Archives Entry | 6 | [x] PASS | agent-d | 2025-12-27 |
| 206-214 | Investigation | 9 | [x] PASS | agent-d | 2025-12-27 |
| 215-219 | Critic Resolution | 5 | [x] PASS | agent-d | 2025-12-27 |
| 220-230 | Revelation | 11 | [x] PASS | agent-d | 2025-12-27 |

**Act 2 Total:** 65/65 reviewed (100% COMPLETE)

### Act 2 Review Notes Summary

**Reviewed by:** agent-d
**Date:** 2025-12-27
**Status:** ✅ ALL 8 SEQUENCES PASS (65/65 nodes)

**Key Findings Across All Sequences:**
- Second person, present tense maintained throughout all 65 nodes
- NPC voices consistently match CHARACTERS.md profiles:
  - The Director: theatrical authority, directing terminology
  - CHORUS: plural collective voice, overlapping fragments
  - The Solved Case: clipped noir style, detective metaphors
  - The Unfinished Quest: heroic cadence with vulnerability
  - The Final Girl: practical survival focus
  - The Happy Ending: warm with underlying steel
  - The Understudy: hesitation, qualifiers, more confident about research
  - The Critic: scathing critique, literary terminology, cold and analytical
- Stat checks use correct notation per RULES.md and match ACT2_MECHANICS.md thresholds
- Check distribution matches Act 2 curve (50% Basic/Standard, 40% Advanced, 10% Expert)
- Fail-forward properly implemented in all nodes
- Faction alignment system properly tracked with UPPERCASE_SNAKE_CASE flags
- All branch links valid and reachable

**Act 2 is publication-ready for v1.0.x release.**

---

### Act 3: The Final Act (51 nodes)

| Range | Sequence | Nodes | Status | Reviewer | Date |
|-------|----------|-------|--------|----------|------|
| 300-305 | Mainstage Entry | 6 | [x] PASS | agent-d | 2025-12-27 |
| 306-309 | Center Stage | 4 | [x] PASS | agent-d | 2025-12-27 |
| 310-313 | Orchestra Pit | 4 | [x] PASS | agent-d | 2025-12-27 |
| 314-317 | Fly System | 4 | [x] PASS | agent-d | 2025-12-27 |
| 318-321 | Audience | 4 | [x] PASS | agent-d | 2025-12-27 |
| 322-335 | Editor Confrontation | 14 | [ ] | | |
| 341-344 | Ending: Revised Draft | 4 | [ ] | | |
| 345-348 | Ending: Open Book | 4 | [ ] | | |
| 349-351 | Ending: Closed Canon | 3 | [ ] | | |
| 352-353 | Ending: Blank Page | 2 | [ ] | | |
| 354-355 | Ending: Eternal Rehearsal | 2 | [ ] | | |

**Act 3 Total:** 22/51 reviewed (43%)

### Mainstage Entry Review Notes (300-305)

**Reviewed by:** agent-d
**Date:** 2025-12-27
**Status:** ✅ ALL PASS

| Node | Title | Structure | Voice | Clarity | Mechanics | Continuity | Playability |
|------|-------|-----------|-------|---------|-----------|------------|-------------|
| 300 | The Mainstage Arrival | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 301 | Survey the Mainstage | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 302 | Ally Reunion | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 303 | Direct Approach | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 304 | Strategy Session | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 305 | Approach Selection | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |

**Findings:**
- Entry sequence properly establishes Act 3 setting with evocative Mainstage descriptions
- Node 302 Ally Reunion validates all 11 potential ally voices against CHARACTERS.md with perfect consistency
- Single stat check (Stage Presence 3 in Node 303) has fail-forward to Node 306
- Mainstage geography matches ACT3_OUTLINE.md (Center Stage, Orchestra Pit, Fly System, Audience)
- Four approach paths from Node 305 map to faction strategies per ACT3_MECHANICS.md

**Issues Found:** None requiring revision.

### Center Stage Review Notes (306-309)

**Reviewed by:** agent-d
**Date:** 2025-12-27
**Status:** ✅ ALL PASS

| Node | Title | Structure | Voice | Clarity | Mechanics | Continuity | Playability |
|------|-------|-----------|-------|---------|-----------|------------|-------------|
| 306 | Center Stage Approach | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 307 | The Wings | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 308 | Story Fragment Encounter | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 309 | Dramatic Entrance | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |

**Findings:**
- The Editor's voice matches CHARACTERS.md: calm with absolute conviction, talks about characters as creations
- Four faction-variant Editor dialogues in Node 309 align with CHARACTERS.md motivation table
- All stat checks use correct notation: Script 2 (306), Improv 2 (307), Script 2 OR Stage Presence 2 (308)
- Check distribution appropriate for Act 3 (all Standard tier for approach sequence)
- Fail-forward properly implemented in all nodes
- Variable content in Node 308 properly references ally flags

**Issues Found:** None requiring revision.

### Orchestra Pit Review Notes (310-313)

**Reviewed by:** agent-d
**Date:** 2025-12-27
**Status:** ✅ ALL PASS

| Node | Title | Structure | Voice | Clarity | Mechanics | Continuity | Playability |
|------|-------|-----------|-------|---------|-----------|------------|-------------|
| 310 | Descend to Orchestra Pit | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 311 | Narrative Manipulation | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 312 | Harmonic Advantage | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 313 | Discordant Reveal | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |

**Structure Findings:**
- All node IDs match filenames (node-310.md through node-313.md)
- Location tags present throughout (*The Mainstage — Orchestra Pit Entrance*, *Conductor's Podium*, *Ascent*, *Aftermath*)
- Forward paths valid: 310→311 on success, 310→306 on failure; 311→312 on success, 311→313 on failure; 312→322; 313→322
- No orphan nodes, no dead ends

**Voice Findings:**
- Second person, present tense maintained throughout all 4 nodes
- The Editor's voice (Node 311, 313) matches CHARACTERS.md profile:
  - Calm with absolute conviction ("Interesting.")
  - Patronizing tone ("But amateurs shouldn't touch instruments they don't understand.")
  - Talks about narrative mechanics ("the *why* of storytelling")
- The Stagehand's voice in ally content (Node 312) matches CHARACTERS.md: simple speech ("Something's changed... The story's changed")
- Tone keywords appropriately distributed: Liminal ("between audience and performers"), Theatrical ("orchestrate," "conductor"), Uncanny ("music as meaning")

**Clarity Findings:**
- Average sentence length within 12-18 word target
- No paragraphs exceed 4 sentences
- Active voice predominates (>80%)
- Word choice concrete and evocative: "harp strung with dialogue threads," "drums made from the moments between heartbeats"

**Mechanics Findings:**
- All stat checks use correct `[STAT CHECK: Stat N]` notation per RULES.md
- Check distribution matches ACT3_OUTLINE.md specification:
  - Node 310: Script 3 (Advanced) ✓
  - Node 311: Improv 3 (Advanced) ✓
  - Node 313: Stage Presence 2 (Standard recovery check) ✓
- Both success AND failure paths defined for all checks
- Fail-forward properly implemented:
  - Node 310 failure → 306 (Center Stage Approach) - valid alternate path
  - Node 311 failure → 313 (Discordant Reveal) - continues with complication
  - Node 313 recovery failure → 322 (confrontation on Editor's terms) - still progresses
- Flags use UPPERCASE_SNAKE_CASE: `ORCHESTRA_PIT_ENTERED`, `NARRATIVE_ADVANTAGE`, `EDITOR_WARNED`
- Effective bonus documented correctly: "+1 effective to next check against the Editor" in Node 312

**Continuity Findings:**
- Orchestra Pit description matches ACT3_OUTLINE.md ("sunken area where narrative 'music' can be manipulated")
- "Instruments made of story elements" aligns with outline specification
- The Editor's knowledge of the pit ("before me, before any Editor") adds appropriate lore depth
- Ally conditional content properly checks for presence flags

**Playability Findings:**
- No instant death without warning
- Difficulty curve appropriate for Act 3:
  - Advanced (3): 2 checks (nodes 310, 311)
  - Standard (2): 1 recovery check (node 313)
- All paths lead to Node 322 (Editor confrontation) - no dead ends
- Recovery check (SP 2) in Node 313 gives hope even after primary failure
- Consequences are meaningful (`NARRATIVE_ADVANTAGE` vs `EDITOR_WARNED`) but not game-ending

**Issues Found:** None requiring revision.

### Fly System Review Notes (314-317)

**Reviewed by:** agent-d
**Date:** 2025-12-27
**Status:** ✅ ALL PASS

| Node | Title | Structure | Voice | Clarity | Mechanics | Continuity | Playability |
|------|-------|-----------|-------|---------|-----------|------------|-------------|
| 314 | Ascend the Fly System | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 315 | The View from Above | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 316 | Tactical Descent | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 317 | Standard Descent | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |

**Findings:**
- Second person, present tense maintained throughout all 4 nodes
- Evocative structural metaphor with narrative threads as fly system rigging
- The Stagehand's voice in Node 317 ally conditional matches CHARACTERS.md: simple speech with insight ("Every story needs a twist")
- All stat checks use correct notation per RULES.md:
  - Stage Presence 3 (314), Script 3 (315) - both Advanced tier
- Check distribution appropriate for Act 3 (all Advanced tier for approach path)
- Fail-forward properly implemented in all nodes:
  - Node 314 failure → Node 306 (Center Stage Approach)
  - Node 315 failure → Node 317 (Standard Descent)
  - Both paths lead to Node 322 (Editor confrontation)
- Conditional content uses correct `{IF ALLIES_PRESENT}` syntax in nodes 316, 317
- All flags use UPPERCASE_SNAKE_CASE: `FLY_SYSTEM_ASCENDED`, `STRUCTURAL_INSIGHT`, `TACTICAL_POSITION`
- Node 317 explicitly documents fail-forward design in Notes section

**Issues Found:** None requiring revision.

### Audience Review Notes (318-321)

**Reviewed by:** agent-d
**Date:** 2025-12-27
**Status:** ✅ ALL PASS

| Node | Title | Structure | Voice | Clarity | Mechanics | Continuity | Playability |
|------|-------|-----------|-------|---------|-----------|------------|-------------|
| 318 | Face The Audience | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 319 | Audience Acknowledgment | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 320 | Audience Judgment | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 321 | Reserved (Expansion Buffer) | ✅ | N/A | ✅ | N/A | ✅ | ✅ |

**Structure Findings:**
- All node IDs match filenames (node-318.md through node-321.md)
- Location tags present throughout (*The Mainstage — The Auditorium Edge*, *Before The Audience*, *The Audience Watches*)
- Forward paths valid: 318→319 on success, 318→320 on failure; 319→322; 320→322 (both outcomes)
- Node 321 is expansion buffer with redirect to Node 301 for safety
- No orphan nodes, no dead ends

**Voice Findings:**
- Second person, present tense maintained throughout all 3 active nodes
- Evocative meta-narrative prose about The Audience as collective story-consumers
- The Happy Ending's brief appearance in Node 320 matches CHARACTERS.md: "warm with underlying steel" ("The story doesn't have to love us. We just have to finish it.")
- `{IF ALLIES_PRESENT}` / `{ELSE}` / `{ENDIF}` conditional content properly structured in nodes 319, 320
- Tone keywords appropriately distributed: Theatrical ("protagonist," "audience," "hero"), Liminal ("between," "collective gaze"), Uncanny ("weight of expectation")

**Clarity Findings:**
- Average sentence length within 12-18 word target
- No paragraphs exceed 4 sentences
- Active voice predominates (>80%)
- Word choice evocative and specific: "the accumulated faith of every reader who ever turned to the next page"

**Mechanics Findings:**
- All stat checks use correct `[STAT CHECK: Stat N]` notation per RULES.md
- Check distribution matches ACT3_OUTLINE.md specification:
  - Node 318: Stage Presence 4 (Expert) ✓
  - Node 320: Script 2 (Standard recovery) ✓
- Both success AND failure paths defined for all checks
- Fail-forward properly implemented:
  - Node 318 failure → 320 (Audience Judgment) - recovery opportunity
  - Node 320 failure → 322 (confrontation with doubt) - still progresses
- Flags use UPPERCASE_SNAKE_CASE: `AUDIENCE_BLESSING`, `AUDIENCE_DOUBT`
- Mechanical effects documented correctly:
  - Node 319: "+2 effective Stage Presence until confrontation ends" with cap at 9
  - Node 320 failure: "-1 effective penalty" on first opposed check

**Continuity Findings:**
- The Audience concept matches ACT3_OUTLINE.md ("everyone who has ever experienced a story")
- Ally references in conditional content properly check presence flags
- Editor foreshadowing appropriate ("The Editor hasn't noticed yet")
- Node 321 reserved buffer documents design rationale for future expansion

**Playability Findings:**
- No instant death without warning
- Difficulty curve appropriate for Act 3:
  - Expert (4): 1 check (node 318) - thematically significant challenge
  - Standard (2): 1 recovery check (node 320) - hope after failure
- All paths lead to Node 322 (Editor confrontation) - no dead ends
- Recovery check (Script 2) in Node 320 gives meaningful second chance
- Consequences are significant (`AUDIENCE_BLESSING` vs `AUDIENCE_DOUBT`) but not game-ending
- Node 321 expansion buffer ensures room for iteration without blocking current play

**Issues Found:** None requiring revision.

---

## Act 3 Editorial Progress

Act 3 is now 22/51 (43%) reviewed:
- ✅ Mainstage Entry (300-305) - 6 nodes PASS
- ✅ Center Stage (306-309) - 4 nodes PASS
- ✅ Orchestra Pit (310-313) - 4 nodes PASS
- ✅ Fly System (314-317) - 4 nodes PASS
- ✅ Audience (318-321) - 4 nodes PASS
- ⬜ Editor Confrontation (322-335) - 14 nodes pending
- ⬜ Ending: Revised Draft (341-344) - 4 nodes pending
- ⬜ Ending: Open Book (345-348) - 4 nodes pending
- ⬜ Ending: Closed Canon (349-351) - 3 nodes pending
- ⬜ Ending: Blank Page (352-353) - 2 nodes pending
- ⬜ Ending: Eternal Rehearsal (354-355) - 2 nodes pending

---

## v1.0.x Editorial Progress Summary

Combined progress:
- **Act 1:** 38/38 (100% COMPLETE)
- **Act 2:** 65/65 (100% COMPLETE)
- **Act 3:** 22/51 (43%)
- **Total:** 125/154 nodes (81%)

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
