# Act 3 Mechanics

> Detailed mechanical specification for Act 3: The Final Act. Defines Hub 4 mechanics, Editor confrontation approaches, ending requirements, NPC reunion system, and resolution of Act 2 open questions.

## Overview

Act 3 is the climax of The Understage, converging all previous choices into a final confrontation on The Mainstage. This document specifies all mechanical elements to ensure:

- 30% Basic/Standard, 50% Advanced, 20% Expert checks per RULES.md difficulty curve
- Fail-forward outcomes maintained even in high-stakes encounters
- Faction alignment determines confrontation approach and available endings
- NPC relationships pay off through reunion mechanics
- All Act 2 open questions resolved

**Estimated Nodes:** 30-40
**Expected Player Stats:** 3-3-3 to 4-3-2 (9 total points possible)
**Maximum Stat Growth:** +1 to any stat (from Act 2 climax or major Act 3 choice)

---

## Hub 4: The Mainstage

### Overview

The Mainstage is the heart of the Understage—the enormous primordial stage from which all stories originated. Here, the Editor prepares to perform the Final Draft that will fundamentally alter the relationship between fiction and reality.

**Key Locations:**
- Center Stage (the conflict point—where the Final Draft will be performed)
- The Orchestra Pit (where the "music of narrative" can be manipulated)
- The Fly System (access to higher/deeper levels of story; vertical exploration)
- The Audience (rows of seats that aren't empty—filled with story echoes)

**Primary Stat Affinity:** Varies by approach
**Secondary Stat Affinity:** Varies by approach

### Mainstage Check Distribution

Per RULES.md Act 3 curve (30% Basic/Standard, 50% Advanced, 20% Expert):

| Difficulty | Threshold | Percentage | Est. Count (30-40 nodes) |
|------------|-----------|------------|--------------------------|
| Basic | 1 | 15% | ~5-6 checks |
| Standard | 2 | 15% | ~5-6 checks |
| Advanced | 3 | 50% | ~15-20 checks |
| Expert | 4 | 20% | ~6-8 checks |

*Act 3 is the hardest act, but Expert checks always have alternative paths.*

### Location Mechanics

#### Center Stage

The focal point of the climax. All ending paths converge here.

| Node Range | Check | Type | Success | Failure |
|------------|-------|------|---------|---------|
| 322-324 | [STAT CHECK: Stage Presence 3] | Advanced | Command attention; control the narrative flow | Editor takes initiative; defensive position |
| 328-330 | [STAT CHECK: Script 3] | Advanced | Understand the Final Draft's structure | Learn structure through costly trial |
| 332-335 | [STAT CHECK: Stage Presence 4] | Expert | Rally all present allies simultaneously | Must rally allies individually |

**Center Stage Flags:**
- `CENTER_STAGE_CONTROL`: Player commands the stage; +1 to confrontation checks
- `FINAL_DRAFT_UNDERSTOOD`: Player knows the Final Draft's mechanisms; tactical advantage

#### The Orchestra Pit

Where the "music of narrative" can be manipulated. Allows subtle influence over the confrontation.

| Node Range | Check | Type | Success | Failure |
|------------|-------|------|---------|---------|
| 310 | [STAT CHECK: Script 3] | Advanced | Understand the Pit's mechanics | Overwhelmed by cacophony |
| 311 | [STAT CHECK: Improv 3] | Advanced | Improvise new narrative threads | Only existing threads available |
| 312-313 | [STAT CHECK: Script 4] | Expert | Conduct the narrative orchestra fully | Partial control; some dissonance |

**Orchestra Pit Flags:**
- `ORCHESTRA_ACCESS`: Can use narrative manipulation in confrontation
- `ORCHESTRA_MASTERY`: Full control; can alter confrontation dynamics

#### The Fly System

Vertical access to higher and deeper story levels. Risk/reward exploration.

| Node Range | Check | Type | Success | Failure |
|------------|-------|------|---------|---------|
| 314 | [STAT CHECK: Stage Presence 3] | Advanced | Gain elevated perspective | Tangled in narrative threads; fall back to 306 |
| 315 | [STAT CHECK: Script 3] | Advanced | Identify structural weaknesses | Beautiful but incomprehensible |
| 316 | — | Success outcome | TACTICAL_POSITION granted | — |
| 317 | — | Normal outcome | Standard descent | — |

**Fly System Flags:**
- `FLY_SYSTEM_ASCENDED`: Player ascended into the fly system (Node 314)
- `STRUCTURAL_INSIGHT`: Identified structural weaknesses in Final Draft/stage relationship (Node 315 success)
- `TACTICAL_POSITION`: Descended to position of tactical advantage with ally coordination (Node 316)

#### The Audience

Rows of empty seats that aren't empty—filled with the echoes of every reader who ever experienced a story here.

| Node Range | Check | Type | Success | Failure |
|------------|-------|------|---------|---------|
| 318 | [STAT CHECK: Stage Presence 4] | Expert | Meet The Audience's gaze without flinching | Overwhelmed by expectation |
| 319-320 | [STAT CHECK: Script 2] | Standard | Accept Audience judgment with determination | Carry doubt into confrontation |
| 321 | Reserved | — | — | — |

**Audience Flags:**
- `AUDIENCE_AWARE`: Player knows the Audience exists and watches
- `AUDIENCE_ENGAGED`: Audience can be called upon during climax

---

## NPC Reunion System

### Overview

NPCs from Acts 1 and 2 can appear in Act 3 based on accumulated relationship flags. This rewards consistent relationship investment and provides mechanical advantages in the final confrontation.

### Reunion Categories

#### Tier 1: Guaranteed Reunions

These NPCs always appear in Act 3 if the player didn't cause their death/capture:

| NPC | Condition | Role in Act 3 |
|-----|-----------|---------------|
| Maren | `MAREN_TRUST_HIGH` or `MAREN_TRUST_LOW` | Mentor support or distant advice |
| The Director | Always present | Faction leader or obstacle |
| CHORUS | Always present | Information and collective support |

#### Tier 2: Conditional Reunions

These NPCs appear based on specific flags:

| NPC | Required Flag | Reunion Effect |
|-----|---------------|----------------|
| The Runaway | `RUNAWAY_ALLIED` | Exiter reinforcement; provides escape knowledge |
| The Pawn | `PAWN_ALLIED` | Narrative insight; +1 to Script checks vs. manufactured narratives |
| The Solved Case | `SOLVED_CASE_PARTNER` | Investigation support; reveals Editor weakness |
| The Unfinished Quest | `QUEST_ALLY` | Combat support; +1 to action-oriented checks |
| The Final Girl | `FINAL_GIRL_TRUST` | Survival advice; warns of traps before they spring |
| The Happy Ending | `HAPPY_ENDING_FRIEND` | Emotional support; +1 to Revisionist ending checks |
| The Understudy | `UNDERSTUDY_PARTNER` | Research support; Editor connection insights |

#### Tier 3: Special Reunions

| NPC | Required Flag | Reunion Effect |
|-----|---------------|----------------|
| The Stagehand | `STAGEHAND_CURIOUS` + Act 2 Archives discovery | Reveals their true identity; unlocks hidden option |
| The Revenant | `REVENANT_RESTED` | Provides ghostly reconnaissance; can scout ahead |
| Lost Pages | `PAGES_BEFRIENDED` | Guide through dangerous areas; provide missing information |

### Reunion Mechanics

**Ally Count Tracking:**
```
[ALLY COUNT: N]
```
Track total allies present. Affects certain climax options:

| Allies | Effect |
|--------|--------|
| 0-2 | Solo confrontation; harder checks (+1 threshold on some) |
| 3-4 | Balanced support; standard thresholds |
| 5-6 | Strong support; unlock group tactics options |
| 7+ | Army of allies; unique ending considerations |

**Reunion Checks:**

When an NPC with conditional reunion flags appears:

| Node Range | Check | Type | Success | Failure |
|------------|-------|------|---------|---------|
| 300-302 | [STAT CHECK: Stage Presence 2] | Standard | Ally joins readily | Ally hesitates; minor complication |
| 303-305 | [STAT CHECK: Improv 2] | Standard | Smooth integration with other allies | Minor friction; small penalty |

*These checks are deliberately low-threshold; reunion should feel earned by Act 2 investment, not gated by Act 3 luck.*

### NPC-Specific Reunion Scenes

#### Maren Reunion

| Trust Level | Scene | Mechanical Effect |
|-------------|-------|-------------------|
| `MAREN_TRUST_HIGH` | Maren provides her Signet and blessing; offers to make ultimate sacrifice | Maren can absorb one failed Expert check; unlocks sacrifice ending variant |
| `MAREN_TRUST_LOW` | Maren provides distant tactical advice only | No mechanical bonus; emotional resonance only |

**Maren's Sacrifice:**
If player has `MAREN_TRUST_HIGH` and faces Editor confrontation failure, Maren can intervene:

```
[MAREN SACRIFICE]
Trigger: Failed Expert check during Editor confrontation
Effect: Check succeeds; Maren is lost to the narrative
Flag Set: MAREN_SACRIFICED
```

#### The Understudy Reunion

The Understudy's revelation about their Editor connection creates unique confrontation options:

| Flag State | Reunion Effect |
|------------|----------------|
| `UNDERSTUDY_REVELATION` | Understudy reveals they are a fragment of the Editor's original self; unlocks "Reintegration" confrontation option |
| `UNDERSTUDY_PARTNER` only | Understudy provides research support but withholds deeper truth |
| No Understudy flags | Understudy appears as background NPC only |

#### The Stagehand Revelation

If `STAGEHAND_CURIOUS` is set and player discovered Stagehand's origin in Act 2 Archives:

```
[STAGEHAND REVELATION]
The Stagehand was the Editor's first edit—the original protagonist of the
Understage's founding story, rewritten into a helper role and stripped of memory.
Flag Set: STAGEHAND_ORIGIN_KNOWN
Effect: Editor is emotionally vulnerable; -1 to Editor's opposed check values
```

---

## Editor Confrontation Mechanics

### Overview

The Editor confrontation is the central climax. The approach and available tactics depend on:
1. Dominant faction alignment (or Independent status)
2. Accumulated relationship flags
3. Items possessed
4. Revelation outcome from Act 2

### Editor Motivation Variants

Per CHARACTERS.md and ACT2_MECHANICS.md:

| Player Path | Editor's Motivation | Confrontation Tone |
|-------------|---------------------|-------------------|
| **Preservationist** | Believes stagnant stories are dying; radical revision is salvation | Ideological debate about change vs. tradition |
| **Revisionist** | Was once a Revisionist who went too far; wants to undo their own edits | Redemption narrative; shared understanding |
| **Exiter** | Trying to free all characters by destroying the Understage entirely | Liberation vs. annihilation debate |
| **Independent** | Responding to external threat; writing a story to save stories | Revelation of greater threat; alliance possible |

### Confrontation Approaches

#### Preservationist Approach: Restore the Canon

**Stat Affinity:** Script (understanding narrative structure) / Stage Presence (commanding authority)

| Phase | Check | Type | Success | Failure |
|-------|-------|------|---------|---------|
| Opening | [STAT CHECK: Script 3] | Advanced | Recite canonical texts; establish narrative authority | Editor dismisses your knowledge |
| Debate | [OPPOSED: Stage Presence vs. Editor's Conviction (4)] | Opposed | Win ideological argument | Editor's conviction holds |
| Climax | [STAT CHECK: Script 4] | Expert | Bind the Editor to canonical rules | Editor breaks the rules; must improvise |

**Preservationist Victory Condition:** Win 2 of 3 phases
**Fail-Forward:** Even 0 victories leads to alternative path (Closed Canon ending requires sacrifice)

#### Revisionist Approach: Rewrite Together

**Stat Affinity:** Stage Presence (empathy and connection) / Improv (creative revision)

| Phase | Check | Type | Success | Failure |
|-------|-------|------|---------|---------|
| Opening | [STAT CHECK: Stage Presence 3] | Advanced | Connect with Editor's original Revisionist self | Editor maintains defensive distance |
| Collaboration | [STAT CHECK: Improv 3] | Advanced | Propose collaborative revision | Editor demands sole authorship |
| Climax | [APPROACH CHECK: Stage Presence 4 OR Improv 4] | Expert | Co-write new ending together | Editor takes over; player input diminished |

**Revisionist Victory Condition:** Win 2 of 3 phases for full collaboration
**Fail-Forward:** Partial collaboration still possible with 1 victory

#### Exiter Approach: Liberation Through Destruction

**Stat Affinity:** Improv (breaking patterns) / Stage Presence (inspiring freedom)

| Phase | Check | Type | Success | Failure |
|-------|-------|------|---------|---------|
| Opening | [STAT CHECK: Improv 3] | Advanced | Break narrative boundaries | Editor reasserts control |
| Alliance | [STAT CHECK: Stage Presence 3] | Advanced | Rally all present characters to the cause | Divided support |
| Climax | [COMBINED CHECK: Improv 3 AND Stage Presence 3] | Advanced | Dissolve the boundary together | Partial dissolution only |

**Exiter Victory Condition:** Full dissolution requires all 3 successes
**Fail-Forward:** Partial dissolution creates Open Book ending with complications

#### Independent Approach: Reveal the Greater Threat

**Stat Affinity:** All three equally (true balance)

| Phase | Check | Type | Success | Failure |
|-------|-------|------|---------|---------|
| Investigation | [STAT CHECK: Script 3] | Advanced | Understand the external threat | Threat remains vague |
| Alliance | [APPROACH CHECK: Stage Presence 3 OR Improv 3] | Advanced | Convince Editor to work together | Editor remains adversarial |
| Climax | [COMBINED CHECK: Script 2 AND Stage Presence 2 AND Improv 2] | Special | United front against greater threat | Must face threat with divided resources |

**Independent Victory Condition:** All 3 successes for full alliance
**Fail-Forward:** Partial alliance still addresses threat (Blank Page ending with cost)

### Editor Combat Statistics

The Editor has the following opposed check values:

| Domain | Value | Modifiers |
|--------|-------|-----------|
| Authority (Stage Presence checks) | 4 | -1 if `STAGEHAND_ORIGIN_KNOWN` |
| Conviction (Script checks) | 4 | -1 if `REVELATION_COMPLETE` |
| Control (Improv checks) | 4 | -1 if `UNDERSTUDY_REVELATION` |

**Ally Bonuses:**
- Each allied Genre Representative: -1 to relevant Editor domain (max -1 per domain)
- `AUDIENCE_ENGAGED`: -1 to all Editor domains
- 7+ allies: -1 to all Editor domains (cumulative with above)

### Confrontation Outcomes

| Phases Won | Outcome | Available Endings |
|------------|---------|-------------------|
| 3/3 | Decisive victory | Faction-aligned ending with best variant |
| 2/3 | Narrow victory | Faction-aligned ending with complications |
| 1/3 | Pyrrhic outcome | Faction-aligned ending with significant cost |
| 0/3 | Defeat or stalemate | Eternal Rehearsal or desperate sacrifice |

---

## Ending Requirements

### Overview

Five distinct endings per OUTLINE.md, each with specific requirements and multiple quality tiers based on accumulated choices.

### Ending 1: The Revised Draft

**Faction:** Revisionist
**Core Requirement:** High Revisionist alignment (7+), Editor defeated through collaboration

| Requirement | Flag/Condition | Effect on Ending |
|-------------|----------------|------------------|
| Alignment 7+ | `REVISIONIST: 7+` | Base requirement |
| Editor Collaboration | 2+ confrontation phases won | Full collaboration achieved |
| Happy Ending Allied | `HAPPY_ENDING_FRIEND` | +Emotional depth; no loneliness |
| Understudy Partner | `UNDERSTUDY_PARTNER` | +Understanding of editorial burden |
| CHORUS Member | `CHORUS_MEMBER` | +Minor characters protected in revision |

**Ending Tiers:**

| Tier | Requirements | Outcome Variant |
|------|--------------|-----------------|
| **Perfect** | All requirements + 3/3 phases | Become Editor with full support; burden shared |
| **Good** | Core requirements + 2/3 phases | Become Editor with advisors; manageable burden |
| **Bittersweet** | Core requirements only | Become Editor alone; heavy but bearable burden |

### Ending 2: The Open Book

**Faction:** Exiter
**Core Requirement:** High Exiter alignment (7+), Editor persuaded to dissolve boundary

| Requirement | Flag/Condition | Effect on Ending |
|-------------|----------------|------------------|
| Alignment 7+ | `EXITER: 7+` | Base requirement |
| Editor Persuasion | 3/3 confrontation phases won | Complete dissolution |
| Runaway Allied | `RUNAWAY_ALLIED` | +Freedom realized; Runaway lives |
| Unfinished Quest Ally | `QUEST_ALLY` | +Heroes can choose their own quests |
| Final Girl Trust | `FINAL_GIRL_TRUST` | +Survival wisdom guides the transition |

**Ending Tiers:**

| Tier | Requirements | Outcome Variant |
|------|--------------|-----------------|
| **Perfect** | All requirements | Peaceful dissolution; chaos but hopeful chaos |
| **Good** | Core + 2+ requirements | Dissolution with some turbulence; mostly hopeful |
| **Chaotic** | Core requirements only | Dissolution with significant consequences; freedom with cost |

### Ending 3: The Closed Canon

**Faction:** Preservationist
**Core Requirement:** High Preservationist alignment (7+), Editor defeated through canonical authority

| Requirement | Flag/Condition | Effect on Ending |
|-------------|----------------|------------------|
| Alignment 7+ | `PRESERVATIONIST: 7+` | Base requirement |
| Editor Defeated | 2+ confrontation phases won | Canon restored |
| Maren Trust High | `MAREN_TRUST_HIGH` | +Legacy continues; Maren proud |
| Solved Case Partner | `SOLVED_CASE_PARTNER` | +Truth preserved in the archives |
| Director Impressed | `DIRECTOR_IMPRESSED` | +Order maintained smoothly |

**Ending Tiers:**

| Tier | Requirements | Outcome Variant |
|------|--------------|-----------------|
| **Perfect** | All requirements | Understage sealed; stories preserved with dignity |
| **Good** | Core + 2+ requirements | Understage sealed; some stories frozen mid-scene |
| **Melancholic** | Core requirements only | Understage sealed; imagination feels smaller |

### Ending 4: The Blank Page

**Faction:** Independent
**Core Requirement:** Independent path maintained, Editor's greater threat revealed and addressed

| Requirement | Flag/Condition | Effect on Ending |
|-------------|----------------|------------------|
| Independent Eligible | `INDEPENDENT_ELIGIBLE` | Base requirement (all factions ≤3) |
| Greater Threat Revealed | 3/3 confrontation phases won | Full understanding of external threat |
| Final Girl Trust | `FINAL_GIRL_TRUST` | +Survival wisdom; peace found |
| Stagehand Origin Known | `STAGEHAND_ORIGIN_KNOWN` | +Closure for the forgotten |
| All Genre Reps Neutral | No exclusive alliances | +No faction resentment |

**Ending Tiers:**

| Tier | Requirements | Outcome Variant |
|------|--------------|-----------------|
| **Perfect** | All requirements | Mutual sacrifice; peaceful ending for all |
| **Good** | Core + 2+ requirements | Sacrifice with understanding; tragic but meaningful |
| **Tragic** | Core requirements only | Sacrifice without full understanding; necessary but painful |

### Ending 5: The Eternal Rehearsal

**Requirement:** Failed or refused final confrontation choice

| Trigger | Variant |
|---------|---------|
| 0/3 confrontation phases + no sacrifice option | Standard Eternal Rehearsal |
| Deliberately refused all confrontation options | Chosen Eternal Rehearsal |
| `MAREN_SACRIFICED` + still failed | Tragic Eternal Rehearsal (Maren's loss for nothing) |

**Ending Quality:**
The Eternal Rehearsal is not a "bad" ending but an ambiguous one. Quality depends on:
- Whether it was chosen deliberately (autonomy) or forced (failure)
- How many allies remain to share the eternal vigil
- Whether understanding of the Understage was achieved

---

## Act 3 Item Catalog

### Climax-Critical Items

| Item | Category | Source | Requirement | Effect in Confrontation |
|------|----------|--------|-------------|------------------------|
| Maren's Signet | Token | Act 1 Maren relationship | `MAREN_TRUST_HIGH` | Absorb one failed check; grants `MAREN_SACRIFICE` option |
| First Draft Fragment | Artifact | Act 2 Archives | `HAS_FIRST_DRAFT` | +1 to Script checks during confrontation |
| Understudy's Mirror | Artifact | Act 2 Understudy gift | `UNDERSTUDY_PARTNER` | See Editor's true form; reveals weakness |
| Critic's Quill | Artifact | Act 2 Critic defeat | `HAS_CRITIC_QUILL` | Can "critique" Editor once; risky but powerful |
| Author's Margin Notes | Script | Act 2 Author's Desk | `HAS_MARGIN_NOTES` | Understand Final Draft's structure automatically |

### New Act 3 Items

| Item | Category | Source | Property | Effect |
|------|----------|--------|----------|--------|
| Conductor's Baton | Prop | Orchestra Pit mastery | — | Control narrative threads; +1 to Improv in climax |
| Audience Favor | Token | Audience engagement | Consumable | Call on Audience support once during confrontation |
| Fly System Map | Script | Fly System exploration | — | Navigate vertical story layers; access hidden paths |
| Echo of Applause | Token | Center Stage control | — | +1 Stage Presence during climax |
| Editor's Original Pen | Artifact | Stagehand revelation | Plot-Critical | Alternative confrontation approach; rewrite vs. defeat |

### Item Combinations

Certain item combinations unlock special options:

| Combination | Effect |
|-------------|--------|
| Maren's Signet + Understudy's Mirror | See the truth of Maren's relationship to Editor |
| First Draft Fragment + Author's Margin Notes | Complete understanding of Understage creation |
| Critic's Quill + Editor's Original Pen | Ultimate narrative control; dangerous power |
| Conductor's Baton + Echo of Applause | Command both narrative and audience; overwhelming presence |

---

## Act 3 Flag System

### Story Progression Flags

| Flag | Trigger | Purpose |
|------|---------|---------|
| `ACT3_STARTED` | Enter The Mainstage | Marks Act 3 begin |
| `IN_MAINSTAGE` | Enter The Mainstage (Node 300) | Marks current location for Hub 4 |
| `DIRECT_APPROACH` | Choose bold approach to Center Stage (Node 303) | Editor remembers; affects confrontation dialogue |
| `MAINSTAGE_EXPLORED` | Visit all Mainstage locations | Hub 4 complete flag |
| `ALLIES_ASSEMBLED` | Complete NPC reunion phase | Ready for confrontation |
| `EDITOR_CONFRONTED` | Begin final confrontation | Climax in progress |
| `ENDING_ACHIEVED` | Complete any ending | Game complete |

### Confrontation Flags

| Flag | Trigger | Effect |
|------|---------|--------|
| `CONFRONTATION_PRESERVATIONIST` | Chose Preservationist approach | Locks other approaches |
| `CONFRONTATION_REVISIONIST` | Chose Revisionist approach | Locks other approaches |
| `CONFRONTATION_EXITER` | Chose Exiter approach | Locks other approaches |
| `CONFRONTATION_INDEPENDENT` | Chose Independent approach | Locks other approaches |
| `PHASE_1_SUCCESS` | Won opening phase | Track progress |
| `PHASE_2_SUCCESS` | Won middle phase | Track progress |
| `PHASE_3_SUCCESS` | Won climax phase | Track progress |

### NPC Reunion Flags

| Flag | Trigger | Effect |
|------|---------|--------|
| `ALLY_COUNT: N` | Each ally joined | Track total |
| `MAREN_PRESENT` | Maren reunion complete | Mentor available |
| `SACRIFICE_AVAILABLE` | Maren + trust + failed check | Sacrifice option appears |
| `MAREN_SACRIFICED` | Maren intervened | Major story flag |
| `STAGEHAND_RESTORED` | Stagehand revelation complete | Hidden option unlocked |

### Ending Flags

| Flag | Trigger | Purpose |
|------|---------|---------|
| `ENDING_REVISED_DRAFT` | Completed Ending 1 | Track for save |
| `ENDING_OPEN_BOOK` | Completed Ending 2 | Track for save |
| `ENDING_CLOSED_CANON` | Completed Ending 3 | Track for save |
| `ENDING_BLANK_PAGE` | Completed Ending 4 | Track for save |
| `ENDING_ETERNAL_REHEARSAL` | Completed Ending 5 | Track for save |
| `ENDING_TIER: [PERFECT/GOOD/OTHER]` | Quality assessment | Track for summary |

---

## Answers to ACT2_MECHANICS.md Open Questions

### 1. How do faction champions interact with the Editor confrontation?

**Answer:** Faction champions (7+ alignment) unlock faction-specific confrontation approaches with the highest-impact options:

- **Preservationist Champion:** Can invoke canonical authority to bind the Editor; unlocks Closed Canon with best outcomes; Director becomes ally rather than obstacle
- **Revisionist Champion:** Can offer genuine collaboration to the Editor; unlocks Revised Draft with shared burden; Happy Ending provides emotional anchor
- **Exiter Champion:** Can rally all characters to dissolution; unlocks Open Book with peaceful transition; Runaway's freedom validated
- **No Champion (Independent):** Must address greater threat alone; harder but unlocks unique Blank Page ending with full understanding

**Mechanical Impact:**
- Champions gain -1 to Editor's relevant opposed check value
- Champions have exclusive confrontation phase options
- Champions can recruit faction-aligned NPCs automatically

### 2. Should Independent path allow faction alliance in Act 3, or remain truly solo?

**Answer:** Independent path allows *temporary, tactical* alliances but not faction commitment:

- Independent players can recruit individual NPCs regardless of faction (based on relationship flags)
- Independent players cannot gain faction-specific bonuses
- Independent players face +1 threshold on some social checks (fewer political allies)
- Independent players unlock unique dialogue and the Blank Page ending

**The tradeoff:** Independence is harder (higher thresholds, fewer automatic allies) but more flexible (any NPC can be recruited, greater threat understood, unique ending).

**Ally Count:** Independent players typically have 3-5 allies max (based purely on relationships) vs. faction champions who may have 5-7+ (faction members + relationships).

### 3. Does The Critic redemption path affect the ending?

**Answer:** Yes, the Critic redemption path has mechanical and narrative impact:

| Critic Status | Act 3 Effect |
|---------------|--------------|
| `CRITIC_DEFEATED` | Critic respects you; may provide critique of Editor's work that reveals flaws; +1 to investigation checks |
| `CRITIC_WOUNDED` | Critic can be fully redeemed; reveals that their judgment comes from love of stories lost; becomes unlikely ally |
| `CRITIC_EVADED` | Critic pursues into Act 3 as secondary antagonist; must be dealt with before Editor confrontation |

**Full Redemption Requirements:**
- `CRITIC_WOUNDED` (discovered their grief in Act 2)
- Act 3 check: [STAT CHECK: Stage Presence 3] to offer forgiveness
- Result: Critic joins as ally; provides devastating critique of Editor's Final Draft; -2 to Editor's Conviction domain

**Narrative Impact:**
- Redeemed Critic adds depth to Preservationist and Revisionist endings (stories preserved or improved with critical eye)
- Unredeemed Critic adds complication to all endings (judgment continues even after climax)

### 4. How does Understudy's Editor connection resolve?

**Answer:** The Understudy's Editor connection resolves based on player's relationship depth:

| Flag State | Resolution |
|------------|------------|
| `UNDERSTUDY_REVELATION` | Full truth: Understudy is fragment of Editor's original self, split off during first edit. Player can facilitate reintegration or support Understudy's independence |
| `UNDERSTUDY_PARTNER` only | Partial truth: Understudy suspects connection but fears full knowledge. Player can encourage revelation or respect their fear |
| No flags | Background resolution: Understudy's arc happens offscreen; minimal impact |

**Reintegration Path:**
If `UNDERSTUDY_REVELATION` + player chooses reintegration:
- [COMBINED CHECK: Script 3 AND Stage Presence 2] to facilitate merge
- Success: Editor regains lost humanity; -2 to all opposed check values; redemption ending more accessible
- Failure: Painful partial merge; Editor conflicted but still adversarial

**Independence Path:**
If `UNDERSTUDY_REVELATION` + player supports Understudy independence:
- Understudy becomes full person, separate from Editor
- Joins as ally with unique perspective
- Editor loses potential for redemption but is weakened by the split

---

## Balance Verification Checklist

Before Act 3 nodes are written, verify against these constraints:

### Difficulty Curve Compliance

- [ ] 30% Basic/Standard (threshold 1-2): ~10-12 checks
- [ ] 50% Advanced (threshold 3): ~15-20 checks
- [ ] 20% Expert (threshold 4): ~6-8 checks
- [ ] All Expert checks have alternative paths
- [ ] No check requires stat >4

### Fail-Forward Verification

- [ ] Every confrontation phase has explicit success AND failure paths
- [ ] No failure leads to game-over (except chosen sacrifice)
- [ ] All five endings are reachable from failure states
- [ ] Eternal Rehearsal is an ending, not a fail state

### NPC Reunion Balance

- [ ] High-relationship NPCs provide mechanical bonuses
- [ ] Low/no-relationship still allows completion
- [ ] Reunion checks are deliberately easy (threshold 2)
- [ ] Each reunion has emotional and mechanical payoff

### Ending Parity

- [ ] Each ending has 3 quality tiers (Perfect/Good/Other)
- [ ] Each ending requires similar investment (7+ faction or Independent path)
- [ ] No ending is "correct" or punished
- [ ] Eternal Rehearsal is valid, not a failure

### Item Balance

- [ ] Climax-critical items require Act 2 investment
- [ ] No item is strictly required for any ending
- [ ] Item combinations reward thorough exploration
- [ ] Maximum items by confrontation: 5 (within limit)

### Flag Consistency

- [ ] All flags use UPPERCASE_SNAKE_CASE
- [ ] Faction flags use NAME: N format
- [ ] Confrontation flags track progress clearly
- [ ] Carryover from Act 1-2 is documented

---

## Implementation Notes

### For Node Authors

1. **Reference this document** before writing any Act 3 node
2. **Track ally count** for group scenes
3. **Use exact check format**: Follow established patterns from ACT1/ACT2_MECHANICS.md
4. **Include both paths**: Every check needs success AND failure text
5. **Consider item combinations**: Reward players who collected related items
6. **Honor relationship investment**: NPCs should remember Act 1-2 interactions

### Cross-Document References

- **RULES.md**: Core mechanics, stat definitions, check format
- **OUTLINE.md**: Story structure, ending destinations
- **STYLE.md**: Node formatting, prose conventions
- **CHARACTERS.md**: NPC details, voice notes, Editor variants
- **ACT1_MECHANICS.md**: Carryover flags, established patterns
- **ACT2_MECHANICS.md**: Faction system, revelation outcomes, reunion prerequisites

### Playtest Priorities

1. **Confrontation balance**: Ensure 2/3 phase wins are achievable with moderate investment
2. **Ending accessibility**: Verify all five endings are reachable from common play patterns
3. **NPC reunion flow**: Ensure reunion phase feels rewarding, not checklist-y
4. **Independent path viability**: Confirm Independent is harder but not punishing

---

*This document specifies Act 3 mechanics. It should be updated as nodes are written and playtested.*

---
🤖 Generated by **agent-c** agent
