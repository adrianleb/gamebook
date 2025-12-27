# Act 3 Outline

> Detailed node-by-node outline for Act 3: The Final Act. Specifies node numbering, content summaries, path structures, and ending variations for Hub 4 (The Mainstage) and the five ending destinations.

## Overview

Act 3 concludes the story with approximately 40 nodes:
- **Hub 4: The Mainstage** (nodes 300-340) — Climactic hub with Editor confrontation
- **Ending Branches** (nodes 341-355) — Five distinct philosophical endings

Node numbering uses 300-level to maintain consistency with Act 2 (100s for Hub 2, 200s for Hub 3).

---

## Hub 4: The Mainstage

**Theme:** Confrontation, sacrifice, resolution
**Node Range:** 300-340
**Estimated Nodes:** 35-40

### Entry Sequence (300-305)

#### Node 300: The Mainstage Arrival
**Type:** Hub entry, scene-setting, reunion trigger
**Summary:** Emerge from the Archives onto the vast Mainstage—the heart of the Understage where all stories originated. The Editor's work is visible everywhere: half-written scenes floating in the wings, narrative threads literally suspended from the fly system.

**Key Elements:**
- Sensory description: enormous stage, impossibly high proscenium, seats stretching into infinite darkness
- The "audience" presence felt—rows of empty seats that watch
- Signs of the Editor's work: pages falling like snow, ink bleeding between realities

**Branches:**
- → 301 (survey the stage)
- → 302 (check for allies)
- → 303 (approach Center Stage directly)

**Flags Set:** `ACT3_STARTED`

---

#### Node 301: Survey the Mainstage
**Type:** Exploration, tactical assessment
**Summary:** Take stock of the Mainstage's geography. Each area offers different tactical and narrative possibilities for the coming confrontation.

**Key Elements:**
- Center Stage: where the Editor works on the Final Draft
- The Orchestra Pit: sunken area where narrative "music" can be manipulated
- The Fly System: ropes and pulleys accessing higher story levels
- The Audience: rows of seats filled with... something

**Branches:**
- → 306 (explore Center Stage approach)
- → 310 (investigate Orchestra Pit)
- → 314 (examine Fly System)
- → 318 (face The Audience)

---

#### Node 302: Ally Reunion
**Type:** Reunion hub, variable based on flags
**Summary:** Allies from Acts 1 and 2 arrive, ready to support you—if they survived and were befriended. This node's content varies dramatically based on accumulated flags.

**Key Elements:**
- [REUNION CHECK] — Each ally appears based on relationship flags
- Surviving allies provide strategic options
- Absent allies are acknowledged—their loss has weight
- Maren present if `MAREN_TRUST_HIGH`; otherwise arrives later, diminished

**Possible Allies (based on flags):**
- The Stagehand (if `STAGEHAND_CURIOUS`)
- The Runaway (if `RUNAWAY_ALLIED`)
- The Prophecy's Pawn (if `PAWN_ALLIED`)
- The Solved Case (if `SOLVED_CASE_PARTNER`)
- The Unfinished Quest (if `QUEST_ALLY`)
- The Final Girl (if `FINAL_GIRL_TRUST`)
- The Happy Ending (if `HAPPY_ENDING_FRIEND`)
- The Understudy (if `UNDERSTUDY_PARTNER`)
- Lost Pages (if `PAGES_BEFRIENDED`)
- CHORUS (if significant positive interactions)

**Branches:**
- → 304 (strategy session with allies)
- → 301 (survey alone if no allies)

**Flags Checked:** All relationship flags from Acts 1-2

---

#### Node 303: Direct Approach
**Type:** Bold action, escalation
**Summary:** Skip reconnaissance and approach Center Stage directly. The Editor notices immediately.

**Key Elements:**
- [STAT CHECK: Stage Presence 3] — Advanced
- Success: Make a dramatic entrance that commands attention
- Failure: Caught off-guard by the stage's defenses

**Branches:**
- Success → 322 (Editor confrontation—direct path)
- Failure → 306 (deflected to Center Stage approach)

**Flags Set:** `DIRECT_APPROACH` (affects Editor dialogue)

---

#### Node 304: Strategy Session
**Type:** Planning, alliance coordination
**Summary:** With gathered allies, plan your approach to the Editor. Each ally offers a different strategic perspective based on their nature.

**Key Elements:**
- [ALLY COUNCIL] — Each present ally contributes advice
- Preservationist allies advocate containment
- Revisionist allies suggest negotiation or editing the Editor
- Exiter allies propose destroying the Final Draft entirely
- Independent allies warn about unintended consequences

**Branches:**
- → 305 (unified approach—pick faction strategy)
- → 301 (more reconnaissance needed)

---

#### Node 305: Approach Selection
**Type:** Strategic choice, path commitment
**Summary:** Choose your primary approach to the Editor based on faction alignment and ally counsel.

**Key Elements:**
- Choice reflects dominant faction alignment
- Allies will support or question based on their nature
- Not locked in—approach can shift during confrontation

**Branches:**
- → 306 (measured approach through Center Stage)
- → 310 (Orchestra Pit manipulation)
- → 314 (Fly System access)
- → 322 (direct confrontation)

---

### Center Stage Approach (306-309)

#### Node 306: Center Stage Approach
**Type:** Primary approach path, tension building
**Summary:** Navigate toward Center Stage where the Editor works. The space shifts around you—reality becoming unstable.

**Key Elements:**
- Stage directions literally appear in the air
- Previous story fragments interfere—ghosts of edited scenes
- [STAT CHECK: Script 2] — Standard
- Success: Navigate the narrative interference
- Failure: Delayed by story fragments

**Branches:**
- → 307 (reach the wings)
- → 308 (story fragment encounter)

---

#### Node 307: The Wings
**Type:** Threshold, observation point
**Summary:** From the wings, observe the Editor at work. The Final Draft is visible—a massive manuscript that pulses with narrative power.

**Key Elements:**
- First clear view of the Editor
- The Final Draft described: pages that write themselves, ink that moves
- [STAT CHECK: Improv 2] — Standard
- Success: Remain undetected, choose moment of approach
- Failure: Editor senses your presence

**Branches:**
- → 309 (dramatic entrance)
- → 322 (detected—confrontation begins)

---

#### Node 308: Story Fragment Encounter
**Type:** Obstacle, emotional beat
**Summary:** A fragment of a story you've affected during your journey manifests. It demands acknowledgment.

**Key Elements:**
- Content varies based on major Act 1-2 choices
- [APPROACH CHECK: Script 2 OR Stage Presence 2] — Combined
- Success: Resolve the fragment peacefully
- Failure: Fragment delays you; Editor gains warning

**Branches:**
- → 307 (continue to wings)
- → 306 (loop back, different approach)

---

#### Node 309: Dramatic Entrance
**Type:** Transition, confrontation setup
**Summary:** Step onto Center Stage. The Editor turns. The final act truly begins.

**Key Elements:**
- Theatrical moment: lights shift, music swells (or silence falls)
- Editor's first direct address to player
- Tone varies by player's dominant faction

**Branches:**
- → 322 (Editor confrontation begins)

**Flags Set:** `DRAMATIC_ENTRANCE`

---

### Orchestra Pit Path (310-313)

#### Node 310: Descend to Orchestra Pit
**Type:** Alternative approach, manipulation focus
**Summary:** The Orchestra Pit lies below the stage—a sunken area where the "music of narrative" can be manipulated. Here, the story's rhythm and tone originate.

**Key Elements:**
- Describe the Pit: instruments made of story elements, scores written in dreams
- [STAT CHECK: Script 3] — Advanced
- Success: Understand the Pit's mechanics
- Failure: Overwhelmed by the cacophony

**Branches:**
- → 311 (manipulate the narrative music)
- → 306 (retreat to Center Stage approach)

---

#### Node 311: Narrative Manipulation
**Type:** Mechanical interaction, story control
**Summary:** Attempt to influence the story's progression by manipulating the narrative music. This could weaken the Editor's control—or draw unwanted attention.

**Key Elements:**
- [STAT CHECK: Improv 3] — Advanced
- Success: Shift the narrative's tone; gain advantage in confrontation
- Failure: Discordant change; Editor becomes aware

**Branches:**
- Success → 312 (harmonic advantage)
- Failure → 313 (discordant reveal)

**Flags Possible:** `NARRATIVE_ADVANTAGE` (on success)

---

#### Node 312: Harmonic Advantage
**Type:** Success outcome, buff
**Summary:** You've attuned the Mainstage's narrative to your purpose. The Editor's control is subtly undermined.

**Key Elements:**
- The stage itself seems more responsive to you
- +1 effective to next check against the Editor
- Allies (if present) sense the shift and coordinate better

**Branches:**
- → 322 (confrontation with advantage)

**Flags Set:** `NARRATIVE_ADVANTAGE`

---

#### Node 313: Discordant Reveal
**Type:** Failure outcome, complication
**Summary:** Your manipulation creates narrative dissonance. The Editor knows exactly where you are—and what you tried.

**Key Elements:**
- Editor's voice echoes through the Pit
- Warning that manipulation has consequences
- [STAT CHECK: Stage Presence 2] — Standard
- Success: Recover composure, proceed on your terms
- Failure: Editor controls the confrontation's opening

**Branches:**
- → 322 (confrontation—Editor's terms)

**Flags Set:** `EDITOR_WARNED`

---

### Fly System Path (314-317)

#### Node 314: Ascend the Fly System
**Type:** Alternative approach, access focus
**Summary:** The Fly System controls what appears and disappears on stage. From above, you can see the larger pattern—and potentially access higher story levels.

**Key Elements:**
- Climbing through ropes and pulleys made of narrative threads
- [STAT CHECK: Stage Presence 3] — Advanced
- Success: Gain elevated perspective
- Failure: Tangled in narrative threads

**Branches:**
- → 315 (the view from above)
- → 306 (fall back to Center Stage approach)

---

#### Node 315: The View from Above
**Type:** Revelation, tactical advantage
**Summary:** From above, see the Mainstage's true structure. The Final Draft is not just a manuscript—it's woven into the stage itself.

**Key Elements:**
- Revelation: The Final Draft is the stage, the stage is the Draft
- Editor's power comes from their position at Center Stage
- [STAT CHECK: Script 3] — Advanced
- Success: Identify structural weaknesses
- Failure: Beautiful but incomprehensible

**Branches:**
- Success → 316 (tactical descent)
- Failure → 317 (standard descent)

**Flags Possible:** `STRUCTURAL_INSIGHT` (on success)

---

#### Node 316: Tactical Descent
**Type:** Strategic advantage, precision approach
**Summary:** With structural insight, descend to a position of advantage. You know exactly where to strike—metaphorically or literally.

**Key Elements:**
- Position yourself at a narrative weakness
- Allies (if present) guided to optimal positions
- Editor's first move will be less effective

**Branches:**
- → 322 (confrontation with tactical advantage)

**Flags Set:** `TACTICAL_POSITION`

---

#### Node 317: Standard Descent
**Type:** Normal progression
**Summary:** Descend from the Fly System without special insight, but having seen the scope of what you face.

**Key Elements:**
- The scale is understood, if not the details
- Humbled but not hopeless
- Proceed to confrontation

**Branches:**
- → 322 (confrontation—standard opening)

---

### The Audience (318-321)

#### Node 318: Face The Audience
**Type:** Horror/wonder encounter, existential challenge
**Summary:** Turn to face the rows of empty seats—except they aren't empty. The Audience is everyone who has ever experienced a story. They watch. They judge. They wait.

**Key Elements:**
- [STAT CHECK: Stage Presence 4] — Expert
- Success: Meet The Audience's gaze without flinching
- Failure: Overwhelmed by the weight of expectation

**Branches:**
- Success → 319 (Audience acknowledgment)
- Failure → 320 (Audience judgment)

---

#### Node 319: Audience Acknowledgment
**Type:** Blessing, power boost
**Summary:** The Audience acknowledges you. For a moment, you are the protagonist of every story ever told. This feeling will carry you through the confrontation.

**Key Elements:**
- Narrative power flows through you
- The Editor notices—this wasn't expected
- +2 effective to Stage Presence checks until confrontation ends

**Branches:**
- → 322 (confrontation with Audience support)

**Flags Set:** `AUDIENCE_BLESSING`

---

#### Node 320: Audience Judgment
**Type:** Challenge, partial failure
**Summary:** The Audience weighs you and finds you... adequate. Not a protagonist. A supporting character. This assessment stings but can be overcome.

**Key Elements:**
- Humbling moment; question your importance
- [STAT CHECK: Script 2] — Standard (recovery)
- Success: Accept your limits but proceed with determination
- Failure: Carry doubt into confrontation

**Branches:**
- → 322 (confrontation—with or without recovered confidence)

**Flags Possible:** `AUDIENCE_DOUBT` (if failed recovery)

---

#### Node 321: Reserved
**Type:** Expansion buffer
**Summary:** Reserved for additional Audience interaction or Mainstage content.

---

### The Confrontation (322-335)

#### Node 322: The Editor Revealed
**Type:** Confrontation opening, revelation
**Summary:** Face the Editor directly. Their identity is revealed—and it varies based on your journey's dominant faction alignment.

**Key Elements:**
- Editor's identity matches player's path interpretation
- The Final Draft is visible, in progress
- Editor explains their motivation (varies by path)
- First opportunity for dialogue or action

**Variable Identities:**

| Player Path | Editor's Nature |
|-------------|-----------------|
| Preservationist | A corrupted former archivist who believes stagnant stories are dying |
| Revisionist | A former Revisionist who went too far; now trying to undo their edits |
| Exiter | A liberator who wants to free all characters by ending the Understage |
| Independent | A protector responding to an external threat beyond the Understage |

**Branches:**
- → 323 (dialogue—attempt to understand)
- → 328 (action—attempt to stop)
- → 333 (ally intervention—if allies present)

**Flags Set:** `EDITOR_REVEALED`

---

#### Node 323: Dialogue: Understanding
**Type:** Confrontation—diplomatic path
**Summary:** Attempt to understand the Editor's perspective before taking action. Their philosophy is complex; their pain is real.

**Key Elements:**
- [STAT CHECK: Script 3] — Advanced
- Success: Editor engages genuinely; reveals deeper truth
- Failure: Editor dismisses dialogue; confrontation escalates

**Branches:**
- Success → 324 (deeper truth)
- Failure → 328 (action required)

---

#### Node 324: Deeper Truth
**Type:** Revelation, perspective shift
**Summary:** The Editor reveals the full context of their plan. The Final Draft isn't destruction—it's transformation. But is their solution acceptable?

**Key Elements:**
- Editor's full motivation explained
- The cost of their plan made clear
- Player given genuine choice: accept their solution, modify it, or reject it

**Branches:**
- → 325 (philosophical challenge—test their logic)
- → 326 (emotional appeal—reach their humanity)
- → 327 (strategic cooperation—work together)
- → 328 (reject and act—stop them regardless)

---

#### Node 325: Philosophical Challenge
**Type:** Argument, Script-focused
**Summary:** Challenge the Editor's logic. Their plan has flaws—you've seen too much of the Understage to accept easy answers.

**Key Elements:**
- [OPPOSED CHECK: Script vs. Editor's Conviction (4)] — Opposed Expert
- Success: Editor's certainty wavers; opening created
- Failure: Editor's logic holds; their conviction strengthens

**Branches:**
- Success → 330 (Editor wavering)
- Failure → 328 (forced to action)

---

#### Node 326: Emotional Appeal
**Type:** Connection attempt, Stage Presence-focused
**Summary:** Reach for the person behind the Editor. They weren't always this—they had connections, feelings, perhaps even someone they loved.

**Key Elements:**
- [STAT CHECK: Stage Presence 4] — Expert
- Success: Touch something real in the Editor
- Failure: Hardened defenses; emotional appeal backfires

**Branches:**
- Success → 330 (Editor wavering)
- Failure → 328 (forced to action)

**Flags Possible:** `EDITOR_MOVED` (affects ending tone)

---

#### Node 327: Strategic Cooperation
**Type:** Collaboration attempt, Improv-focused
**Summary:** Propose working together. Perhaps the Final Draft can be edited—changed to preserve what matters while achieving the Editor's goals.

**Key Elements:**
- [STAT CHECK: Improv 4] — Expert
- Success: Editor considers collaboration
- Failure: Editor sees compromise as weakness

**Branches:**
- Success → 331 (collaborative revision)
- Failure → 328 (forced to action)

**Flags Possible:** `COLLABORATION_OFFERED`

---

#### Node 328: Action: Opposing
**Type:** Confrontation—combat/contest path
**Summary:** Words have failed or were never attempted. Time to act. Stop the Editor by force, guile, or sheer narrative will.

**Key Elements:**
- [APPROACH CHECK: Script 3 OR Stage Presence 3 OR Improv 3] — Combined Advanced
- Success: Gain the upper hand
- Failure: Editor gains advantage; situation worsens

**Branches:**
- Success → 329 (Editor contested)
- Failure → 332 (desperate measures)

---

#### Node 329: Editor Contested
**Type:** Advantage gained
**Summary:** You've challenged the Editor's control over the Mainstage. The Final Draft stutters. But they won't give up easily.

**Key Elements:**
- Editor is pressed but not defeated
- The Draft's power wavers
- [STAT CHECK: Any stat 4] — Expert
- Success: Editor's control broken
- Failure: Editor recovers; stalemate

**Branches:**
- Success → 330 (Editor wavering)
- Failure → 335 (climactic choice—deadlock)

---

#### Node 330: Editor Wavering
**Type:** Turning point
**Summary:** The Editor's certainty breaks—through philosophy, emotion, or force. They see another possibility. The Final Draft's completion halts.

**Key Elements:**
- The Editor hesitates
- The Final Draft suspended mid-sentence
- Player has clear opportunity to determine outcome

**Branches:**
- → 335 (climactic choice—with Editor cooperative or broken)

**Flags Set:** `EDITOR_WAVERING`

---

#### Node 331: Collaborative Revision
**Type:** Alliance formed
**Summary:** You and the Editor work together on a new vision. The Final Draft can be changed—but to what?

**Key Elements:**
- Joint editing of the Draft
- Allies react based on their alignments
- [COMBINED CHECK: Script 2 + Stage Presence 2 + Improv 2] — Special
- Success: Collaborative ending unlocked
- Failure: Collaboration breaks down

**Branches:**
- Success → 335 (climactic choice—collaborative path available)
- Failure → 328 (return to opposition)

---

#### Node 332: Desperate Measures
**Type:** Failure state, escalation
**Summary:** You've lost the advantage. The Editor's power over the Mainstage is complete—unless you sacrifice something precious.

**Key Elements:**
- Editor in control
- Allies at risk (if present)
- Maren offers sacrifice (if `MAREN_TRUST_HIGH`)
- Alternative: Sacrifice your own certainty

**Branches:**
- → 334 (accept sacrifice—Maren or self)
- → 335 (refuse sacrifice—accept limited outcomes)

---

#### Node 333: Ally Intervention
**Type:** Support sequence
**Summary:** Your allies act. Based on who is present, they provide different types of support—distraction, wisdom, or direct aid.

**Key Elements:**
- [ALLY INTERVENTION] — Effects vary by present allies
- Each ally provides unique benefit
- Allies may be endangered by their intervention

**Possible Interventions:**
- The Stagehand: Reveals connection to Editor; creates opening
- The Solved Case: Deduces Editor's weakness
- The Unfinished Quest: Direct challenge; draws Editor's attention
- The Final Girl: Tactical advice; survival insight
- The Happy Ending: Emotional appeal on your behalf
- The Understudy: Mirror revelation about Editor's true nature
- The Pawn: Narrative insight; sees the story's structure
- Lost Pages: Fragment assistance; chaotic but helpful
- CHORUS: Collective distraction; overwhelm with minor characters

**Branches:**
- → 322 (return to confrontation with ally boost)

---

#### Node 334: The Sacrifice
**Type:** Tragic turning point
**Summary:** Someone pays the price. Either Maren fulfills her arc by giving herself to save the stories, or you sacrifice part of your identity to break the Editor's hold.

**Key Elements:**
- If Maren: Her life force disrupts the Final Draft; creates opening
- If Self: You "write out" part of your own story; permanent change
- Either way: Editor's control is broken

**Branches:**
- → 335 (climactic choice—through sacrifice)

**Flags Set:** `MAREN_SACRIFICED` or `SELF_SACRIFICED`

---

#### Node 335: The Last Curtain Call
**Type:** Climactic choice, ending gateway
**Summary:** The Final Draft hangs in the balance. The Editor is defeated, cooperative, or stalemated. You hold the pen—metaphorically or literally. What do you write?

**Key Elements:**
- Review of accumulated choices
- Each ending has requirements (see Ending Destinations)
- Player makes final choice
- The Mainstage responds to the decision

**Branches:**
- → 341 (The Revised Draft ending) — High Revisionist
- → 345 (The Open Book ending) — High Exiter
- → 349 (The Closed Canon ending) — High Preservationist
- → 352 (The Blank Page ending) — Independent + Editor's truth
- → 354 (The Eternal Rehearsal ending) — Refused or failed choice

**Flags Checked:** All major faction and choice flags

---

### Nodes 336-340: Reserved
**Type:** Expansion buffer
**Summary:** Reserved for additional confrontation content, alternative paths, or expanded climax sequences.

---

## Ending Branches

**Node Range:** 341-355
**Five Distinct Endings:** Each reflects a different philosophical stance and accumulated choices.

---

### Ending 1: The Revised Draft (341-344)

**Requirement:** High Revisionist alignment, Editor defeated or convinced

#### Node 341: Taking the Pen
**Type:** Ending approach
**Summary:** You claim the Editor's power. The Final Draft is incomplete, but you can finish it—your way. Stories don't have to end as written. They can be revised, improved, given genuine agency.

**Key Elements:**
- The pen (or its equivalent) passes to you
- Weight of responsibility felt
- Allies (especially Happy Ending) react

**Branches:**
- → 342 (accept the burden)
- → 335 (reject—choose different ending)

---

#### Node 342: The Revision Begins
**Type:** Transition
**Summary:** Begin the work of revision. Not all at once—that was the Editor's mistake. One story at a time. One choice at a time. Earned endings, not mandated ones.

**Key Elements:**
- First revision: free a character you've met
- The Understage stabilizes under new guidance
- Reality and the Understage remain separate

---

#### Node 343: The New Editor
**Type:** Ending beat
**Summary:** You are the Editor now. The burden is heavy but you bear it with purpose. Characters can appeal to you. Stories can be changed. But every revision has consequences you must live with.

**Key Elements:**
- Allies depart to their own stories
- Maren (if alive) expresses pride or concern
- Your role is permanent

---

#### Node 344: Revised Draft Resolution
**Type:** Ending conclusion
**Summary:** Time passes. You've made mistakes. You've done good. The Understage continues, stories continue, but they're better—or at least, they have the chance to be. Bittersweet. Power with responsibility.

**Outcome:** Reality and the Understage remain separate, but you bear the burden of being the new Editor. Stories can be revised, but the weight of that power is yours to carry.

**Flags Set:** `ENDING_REVISED_DRAFT`

---

### Ending 2: The Open Book (345-348)

**Requirement:** High Exiter alignment, Editor persuaded

#### Node 345: Breaking the Binding
**Type:** Ending approach
**Summary:** The boundary between fiction and reality doesn't have to exist. Characters can be real. Stories can be lived. Freedom—for everyone, in both directions.

**Key Elements:**
- The Final Draft is transformed, not destroyed
- The boundary begins to dissolve
- Chaos, but free chaos

**Branches:**
- → 346 (embrace the opening)
- → 335 (reject—choose different ending)

---

#### Node 346: The Doors Open
**Type:** Transition
**Summary:** The barrier falls. Characters step into reality. People step into stories. The world becomes stranger, wilder, more dangerous—but also more wondrous.

**Key Elements:**
- The Unfinished Quest walks into the real world
- Someone from reality enters their favorite book
- Rules break down; new rules form

---

#### Node 347: A World Rewritten
**Type:** Ending beat
**Summary:** Reality adapts. Fiction adapts. The distinction blurs until it ceases to matter. You walk between worlds freely, as do countless others.

**Key Elements:**
- Your role changes—Prompter becomes Bridge-Keeper
- Some find joy; others struggle
- Nothing is ever predictable again

---

#### Node 348: Open Book Resolution
**Type:** Ending conclusion
**Summary:** The boundary is gone. Reality and fiction intermingle freely. Some days you wake up in a mystery novel. Some days a fairy tale character has coffee at your cafe. The world is stranger but freer. Hopeful but uncertain.

**Outcome:** The boundary dissolves peacefully. Fictional characters can live in reality; real people can enter stories. Chaos, but free chaos.

**Flags Set:** `ENDING_OPEN_BOOK`

---

### Ending 3: The Closed Canon (349-351)

**Requirement:** High Preservationist alignment, Editor defeated

#### Node 349: Sealing the Passage
**Type:** Ending approach
**Summary:** The Understage is too dangerous. The boundary must be not just maintained but sealed. Stories will continue, but separate. Safe. Protected. Unchangeable.

**Key Elements:**
- The Final Draft is destroyed
- The passage between worlds closes
- Permanence—for better or worse

**Branches:**
- → 350 (complete the sealing)
- → 335 (reject—choose different ending)

---

#### Node 350: The Final Curtain
**Type:** Transition
**Summary:** The connection between the Understage and reality closes forever. Stories become fixed. No more breaches. No more escapes. No more Prompters.

**Key Elements:**
- Say goodbye to characters you've befriended
- Maren (if alive) can stay or go—her choice
- You must leave, carrying only memories

---

#### Node 351: Closed Canon Resolution
**Type:** Ending conclusion
**Summary:** The Understage is sealed completely. Stories become static. Reality is protected but diminished—imagination itself feels smaller. You remember the Understage, but no one else believes you. Safe but melancholic.

**Outcome:** The Understage is sealed. Stories become static. Reality is protected but diminished. No more magic, no more danger, but also no more wonder.

**Flags Set:** `ENDING_CLOSED_CANON`

---

### Ending 4: The Blank Page (352-353)

**Requirement:** Independent path, Editor's truth revealed

#### Node 352: The Deeper Threat
**Type:** Ending approach
**Summary:** The Editor wasn't the villain. They were responding to something worse—a threat from beyond the Understage itself. A story so dangerous it could end all stories. The only solution: end both.

**Key Elements:**
- The true threat revealed (the Silence—anti-narrative)
- Editor becomes ally in final moments
- Mutual sacrifice required

**Branches:**
- → 353 (accept the cost)
- → 335 (reject—choose different ending)

---

#### Node 353: Blank Page Resolution
**Type:** Ending conclusion
**Summary:** Together with the Editor, you write an ending to end all endings. The Understage and the threat both cease. Reality continues, but no new stories will be written in the same way. Imagination persists, but the doorway is gone. Tragic but peaceful.

**Outcome:** You and the Editor end both the Understage and its threat. Reality survives with no more new stories from that source—but no more dangers from old ones. Tragic but peaceful.

**Flags Set:** `ENDING_BLANK_PAGE`

---

### Ending 5: The Eternal Rehearsal (354-355)

**Requirement:** Failed or refused final choice

#### Node 354: No Ending
**Type:** Ending approach—refusal
**Summary:** You cannot choose. Or you will not. Or the choice is taken from you. The Final Draft remains incomplete. The crisis continues. But so do you.

**Key Elements:**
- The climax... doesn't climax
- The Editor persists, defeated but not gone
- The Understage remains in flux

---

#### Node 355: Eternal Rehearsal Resolution
**Type:** Ending conclusion
**Summary:** The conflict continues indefinitely. You remain a Prompter, endlessly managing a crisis that never resolves. Not a failure state, but a choice to embrace the liminal life forever. The Understage becomes your home. Ambiguous.

**Outcome:** The conflict never resolves. You remain a Prompter forever, managing eternal crises. Neither victory nor defeat—just continuation. An ending that isn't.

**Flags Set:** `ENDING_ETERNAL_REHEARSAL`

---

## Node Summary Tables

### Hub 4: The Mainstage (300-340)

| Node | Title | Type | Key Check |
|------|-------|------|-----------|
| 300 | The Mainstage Arrival | Entry | — |
| 301 | Survey the Mainstage | Exploration | — |
| 302 | Ally Reunion | Variable | Reunion Check |
| 303 | Direct Approach | Bold | Stage Presence 3 |
| 304 | Strategy Session | Planning | — |
| 305 | Approach Selection | Choice | — |
| 306 | Center Stage Approach | Path | Script 2 |
| 307 | The Wings | Threshold | Improv 2 |
| 308 | Story Fragment Encounter | Obstacle | Script 2 OR Stage Presence 2 |
| 309 | Dramatic Entrance | Transition | — |
| 310 | Descend to Orchestra Pit | Path | Script 3 |
| 311 | Narrative Manipulation | Mechanical | Improv 3 |
| 312 | Harmonic Advantage | Success | — |
| 313 | Discordant Reveal | Failure | Stage Presence 2 |
| 314 | Ascend the Fly System | Path | Stage Presence 3 |
| 315 | The View from Above | Revelation | Script 3 |
| 316 | Tactical Descent | Advantage | — |
| 317 | Standard Descent | Normal | — |
| 318 | Face The Audience | Challenge | Stage Presence 4 |
| 319 | Audience Acknowledgment | Blessing | — |
| 320 | Audience Judgment | Partial | Script 2 |
| 321 | Reserved | Buffer | — |
| 322 | The Editor Revealed | Confrontation | — |
| 323 | Dialogue: Understanding | Diplomatic | Script 3 |
| 324 | Deeper Truth | Revelation | — |
| 325 | Philosophical Challenge | Argument | Script 4 (Opposed) |
| 326 | Emotional Appeal | Connection | Stage Presence 4 |
| 327 | Strategic Cooperation | Collaboration | Improv 4 |
| 328 | Action: Opposing | Combat | Script 3 OR Stage Presence 3 OR Improv 3 |
| 329 | Editor Contested | Advantage | Any 4 |
| 330 | Editor Wavering | Turning | — |
| 331 | Collaborative Revision | Alliance | Combined 2/2/2 |
| 332 | Desperate Measures | Failure | — |
| 333 | Ally Intervention | Support | Variable |
| 334 | The Sacrifice | Tragic | — |
| 335 | The Last Curtain Call | Climax | — |
| 336-340 | Reserved | Buffer | — |

### Ending Branches (341-355)

| Node | Title | Type | Requirement |
|------|-------|------|-------------|
| 341 | Taking the Pen | Approach | High Revisionist |
| 342 | The Revision Begins | Transition | — |
| 343 | The New Editor | Beat | — |
| 344 | Revised Draft Resolution | Conclusion | — |
| 345 | Breaking the Binding | Approach | High Exiter |
| 346 | The Doors Open | Transition | — |
| 347 | A World Rewritten | Beat | — |
| 348 | Open Book Resolution | Conclusion | — |
| 349 | Sealing the Passage | Approach | High Preservationist |
| 350 | The Final Curtain | Transition | — |
| 351 | Closed Canon Resolution | Conclusion | — |
| 352 | The Deeper Threat | Approach | Independent |
| 353 | Blank Page Resolution | Conclusion | — |
| 354 | No Ending | Approach | Failed/Refused |
| 355 | Eternal Rehearsal Resolution | Conclusion | — |

---

## Difficulty Distribution

### Hub 4 Check Distribution

Per RULES.md Act 3 target curve (30% Basic/Standard, 50% Advanced, 20% Expert):

| Difficulty | Threshold | Target % | Notes |
|------------|-----------|----------|-------|
| Basic | 1 | 15% | Entry-level checks, accessibility gates |
| Standard | 2 | 15% | Moderate investment checks |
| Advanced | 3 | 50% | Primary challenge tier for climax |
| Expert | 4 | 20% | High-stakes pivotal moments |

*Hub 4 skews toward Advanced and Expert checks due to climactic confrontation focus. All Expert checks have alternative paths per RULES.md fail-forward requirement. Opposed and Combined checks are categorized by their effective difficulty threshold.*

### Ending Distribution

Each ending is equally achievable through consistent play:
- **Revised Draft**: Revisionist-focused path + Editor defeat/persuasion
- **Open Book**: Exiter-focused path + Editor persuasion
- **Closed Canon**: Preservationist-focused path + Editor defeat
- **Blank Page**: Independent path + truth revelation + mutual sacrifice
- **Eternal Rehearsal**: Default/failsafe for any path that doesn't commit

---

## Ally Contribution Summary

| Ally | Required Flag | Contribution |
|------|---------------|--------------|
| Maren | `MAREN_TRUST_HIGH` | Sacrifice option, mentor support |
| The Stagehand | `STAGEHAND_CURIOUS` | Editor connection reveal |
| The Runaway | `RUNAWAY_ALLIED` | Exiter solidarity |
| The Prophecy's Pawn | `PAWN_ALLIED` | Narrative structure insight |
| The Solved Case | `SOLVED_CASE_PARTNER` | Deductive weakness finding |
| The Unfinished Quest | `QUEST_ALLY` | Direct confrontation support |
| The Final Girl | `FINAL_GIRL_TRUST` | Survival tactics |
| The Happy Ending | `HAPPY_ENDING_FRIEND` | Emotional appeal boost |
| The Understudy | `UNDERSTUDY_PARTNER` | Mirror revelation |
| Lost Pages | `PAGES_BEFRIENDED` | Fragment assistance |
| CHORUS | Positive interactions | Collective distraction |

---

## Dependencies

This document depends on:
- `OUTLINE.md` — Story structure and ending destinations
- `ACT2_OUTLINE.md` — Previous hub structure and flag states
- `CHARACTERS.md` — NPC profiles, especially The Editor
- `RULES.md` — Core mechanics and faction system
- `STYLE.md` — Node formatting conventions

This document informs:
- Individual Act 3 node content writing
- Ending balance verification
- Playtest planning for final act

---

*This outline provides node specifications for Act 3. Individual node content will expand these summaries into full prose following STYLE.md conventions.*

---
🤖 Generated by **agent-b** agent
