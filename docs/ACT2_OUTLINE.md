# Act 2 Outline

> Detailed node-by-node outline for Act 2: The Descent. Specifies node numbering, content summaries, path structures, and faction variations for Hub 2 (The Green Room) and Hub 3 (The Archives).

## Overview

Act 2 expands into two major hubs with approximately 80 nodes total:
- **Hub 2: The Green Room** (nodes 100-140) — Social-political hub with faction dynamics
- **Hub 3: The Archives** (nodes 200-240) — Investigative hub leading to the Revelation

Node numbering uses 100-level gaps to allow future expansion without renumbering.

---

## Hub 2: The Green Room

**Theme:** Alliance-building, faction politics, social navigation
**Node Range:** 100-140
**Estimated Nodes:** 35-40

### Entry Sequence (100-105)

#### Node 100: Green Room Arrival
**Type:** Hub entry, scene-setting
**Summary:** Player descends from the First Crossing into the Green Room—a vast backstage lounge where characters from countless stories mingle in uneasy coexistence. Establish the neutral territory concept.

**Key Elements:**
- Sensory description: mismatched furniture from different genres, lighting that shifts between scenes
- First glimpse of CHORUS in the background
- The Director's presence noted but not engaged

**Branches:**
- → 101 (approach The Director)
- → 102 (explore the Main Lounge)
- → 103 (observe from the edges)

**Flags Set:** `ACT2_STARTED`

---

#### Node 101: The Director's Introduction
**Type:** NPC introduction, first impression
**Summary:** The Director acknowledges the player's arrival. First test of how you present yourself.

**Key Elements:**
- [STAT CHECK: Stage Presence 2] — Standard
- Success: Director acknowledges you as worthy of attention, offers guidance
- Failure: Director dismisses you to underlings, must prove yourself

**Branches:**
- Success → 104 (Director's briefing)
- Failure → 102 (explore independently)

**Flags Possible:** `DIRECTOR_IMPRESSED` (on success)

---

#### Node 102: Main Lounge Exploration
**Type:** Exploration, NPC discovery
**Summary:** Navigate the Main Lounge, observing faction representatives and CHORUS. Multiple opportunities for first impressions.

**Key Elements:**
- Describe the Call Board (quest hooks visible)
- Genre Representatives visible in their corners
- CHORUS moves through, offering fragments of information

**Branches:**
- → 106 (approach The Solved Case)
- → 107 (approach The Unfinished Quest)
- → 108 (approach The Final Girl)
- → 109 (approach The Happy Ending)
- → 103 (approach CHORUS)

---

#### Node 103: CHORUS Contact
**Type:** NPC interaction, information gathering
**Summary:** CHORUS approaches or is approached. They offer information about the Green Room's dynamics.

**Key Elements:**
- [STAT CHECK: Improv 1] — Basic
- Success: CHORUS welcomes you, shares minor faction information
- Failure: CHORUS ignores you, must earn their attention elsewhere

**Branches:**
- → 102 (return to exploration)
- → 110 (CHORUS rumor hook)

**Flags Possible:** `CHORUS_ALLY` (if helped later)

---

#### Node 104: Director's Briefing
**Type:** Exposition, faction overview
**Summary:** The Director provides official orientation to the Green Room. Learn about faction dynamics from the Preservationist perspective.

**Key Elements:**
- Faction overview (biased toward Preservationist view)
- Warning about "unstable elements" (Exiters)
- Mention of disturbances in the Archives
- Offer of Director's patronage (at a cost)

**Branches:**
- → 105 (accept Director's guidance) — Sets Preservationist +1
- → 102 (decline, explore independently)

**Flags Possible:** `DIRECTOR_SUSPICIOUS` (if you challenge them here)

---

#### Node 105: Call Board Discovery
**Type:** Quest hub, choice point
**Summary:** The Call Board displays current "situations" requiring attention. Each represents a faction-aligned quest.

**Key Elements:**
- Preservationist notice: "Escaped character sighting—containment needed"
- Revisionist notice: "Story fragment corrupted—assistance requested"
- Exiter notice: "Safe passage required—discrete help wanted"
- Neutral notice: "The Archives seek researchers"

**Branches:**
- → 115 (Preservationist quest line)
- → 120 (Revisionist quest line)
- → 125 (Exiter quest line)
- → 130 (Archives approach—neutral path)

---

### Genre Representative Encounters (106-114)

#### Node 106: The Solved Case
**Type:** NPC deep interaction, Preservationist contact
**Summary:** Engage with the noir detective. They're solving a case about missing story fragments.

**Key Elements:**
- [STAT CHECK: Script 2] — Standard
- Success: Present your case logically, earn respect
- Failure: Dismissed as amateur, must prove investigative worth

**Branches:**
- Success → 111 (join investigation)
- Failure → 102 (return to lounge)

**Flags Possible:** `SOLVED_CASE_RESPECT`

---

#### Node 107: The Unfinished Quest
**Type:** NPC deep interaction, Exiter contact
**Summary:** The restless hero seeks worthy companions. Test of heroic presence.

**Key Elements:**
- [STAT CHECK: Stage Presence 2] — Standard
- Success: Recognized as fellow protagonist
- Failure: Seen as supporting character, limited access

**Branches:**
- Success → 112 (heroic alliance offer)
- Failure → 102 (return to lounge)

**Flags Possible:** `QUEST_INSPIRED`

---

#### Node 108: The Final Girl
**Type:** NPC deep interaction, Independent contact
**Summary:** The survivor watches from the edges. Approach must feel genuine, not scripted.

**Key Elements:**
- [STAT CHECK: Improv 2] — Standard
- Success: She shares survival wisdom, hints about danger
- Failure: Generic advice only, guards remain up

**Branches:**
- Success → 113 (survival lessons)
- Failure → 102 (return to lounge)

**Flags Possible:** `FINAL_GIRL_TRUST` (requires multiple interactions)

---

#### Node 109: The Happy Ending
**Type:** NPC deep interaction, Revisionist contact
**Summary:** The romance lead shares their philosophy of earned endings. Emotional but analytical.

**Key Elements:**
- [STAT CHECK: Stage Presence 1] — Basic
- Success: Pleasant conversation, invitation to Revisionist gathering
- Failure: Polite but distant, surface-level only

**Branches:**
- Success → 114 (Revisionist philosophy)
- Failure → 102 (return to lounge)

**Flags Possible:** `HAPPY_ENDING_FRIEND`

---

#### Node 110: CHORUS Rumor Hook
**Type:** Information gathering, mystery setup
**Summary:** CHORUS shares a rumor about disturbances in the Archives. Someone is "editing" things that shouldn't be edited.

**Key Elements:**
- [STAT CHECK: Stage Presence 2] — Standard
- Success: CHORUS shares useful rumor about the Editor
- Failure: Generic information only

**Branches:**
- → 105 (to Call Board with new knowledge)
- → 130 (directly to Archives approach)

---

#### Node 111: Investigation Partner
**Type:** Quest advancement, Preservationist path
**Summary:** The Solved Case accepts you as partner. Work together to track missing story fragments.

**Key Elements:**
- [STAT CHECK: Script 3] — Advanced
- Success: Solve their puzzle together, gain information about Archives
- Failure: They solve it for you, no reward but path continues

**Branches:**
- → 116 (Preservationist quest continues)
- → 130 (Archives approach unlocked)

**Flags Set:** `SOLVED_CASE_PARTNER`

---

#### Node 112: Heroic Alliance
**Type:** Quest advancement, Exiter path
**Summary:** The Unfinished Quest offers to join forces. A quest that actually matters—helping someone escape.

**Key Elements:**
- [STAT CHECK: Improv 2] — Standard
- Success: Suggest new narrative possibility, inspire action
- Failure: Offer only familiar tropes, they remain contemplative

**Branches:**
- → 126 (Exiter quest continues)
- → 102 (return if failed)

**Flags Possible:** `QUEST_ALLY`

---

#### Node 113: Survival Lessons
**Type:** Quest advancement, Independent path
**Summary:** The Final Girl teaches you how to read danger in the Understage. Practical survival skills.

**Key Elements:**
- [STAT CHECK: Script 2] — Standard
- Success: Recognize her pattern-breaking nature, understand Independent path
- Failure: Miss the significance, surface-level tips only

**Branches:**
- → 118 (Independent path revelation)
- → 102 (return to lounge)

**Flags Possible:** `INDEPENDENT_PATH_OPEN` (if all factions low)

---

#### Node 114: Revisionist Philosophy
**Type:** Quest advancement, Revisionist path
**Summary:** The Happy Ending explains Revisionist ideology. Stories should be edited to give characters genuine agency.

**Key Elements:**
- [STAT CHECK: Script 3] — Advanced
- Success: Understand revision philosophy deeply
- Failure: Simplistic understanding, limited access

**Branches:**
- → 121 (Revisionist quest continues)
- → 102 (return to lounge)

**Flags Possible:** `REVISIONIST_INSIDER`

---

### Faction Quest Lines (115-129)

#### Node 115: Preservationist Mission Briefing
**Type:** Quest start, faction commitment
**Summary:** The Solved Case and Director assign a mission: track down a character causing instability.

**Key Elements:**
- Target: A story fragment that's "bleeding" between narratives
- Stakes: If unchecked, multiple stories could collapse
- Method: Contain and return, not destroy

**Branches:**
- → 116 (accept mission)
- → 105 (decline, return to Call Board)

**Flags Set:** `PRESERVATIONIST: +1`

---

#### Node 116: The Bleeding Fragment
**Type:** Quest execution, investigation
**Summary:** Track the fragment through the Green Room's margins. It's hiding in the Dressing Rooms.

**Key Elements:**
- [STAT CHECK: Script 2] — Standard
- Success: Locate fragment efficiently
- Failure: Fragment moves, chase continues

**Branches:**
- → 117 (confront fragment)
- → 116 (loop if failed—different approach)

---

#### Node 117: Fragment Confrontation
**Type:** Quest climax, moral choice
**Summary:** The fragment is a child character from a story that was never finished. They're terrified.

**Key Elements:**
- [APPROACH CHECK: Stage Presence 2 OR Script 2] — Combined
- Success: Calm the fragment, learn about the Archives threat
- Failure: Fragment panics, partial information only

**Branches:**
- → 119 (return fragment to story) — Preservationist +2
- → 127 (help fragment hide) — Exiter +2, Preservationist -2
- → 130 (Archives approach with fragment's intel)

---

#### Node 118: Independent Revelation
**Type:** Path unlock, faction bypass
**Summary:** The Final Girl reveals the truth: factions are all performing for the Director. True freedom means trusting no ideology.

**Key Elements:**
- [APPROACH CHECK: Improv 3 OR Script 3] — Combined
- Success: She reveals the Director's secret—they're not neutral
- Failure: Hints only, must discover independently

**Branches:**
- → 130 (Archives approach as Independent)
- → 105 (return to Call Board with new perspective)

**Flags Set:** `INDEPENDENT_ELIGIBLE` (if all factions ≤3)

---

#### Node 119: Preservationist Resolution
**Type:** Quest completion, faction reward
**Summary:** Return the fragment to a suitable story. The Solved Case approves. The Director takes note.

**Key Elements:**
- Fragment placed in stable narrative
- Director offers access to restricted areas
- Solved Case offers ongoing partnership

**Branches:**
- → 130 (Archives approach)
- → 105 (more Green Room quests)

**Flags Set:** `PRESERVATIONIST: +2`, `HAS_DIRECTOR_SIGIL`

---

#### Node 120: Revisionist Mission Briefing
**Type:** Quest start, faction commitment
**Summary:** The Happy Ending and CHORUS need help. A story is stuck in a loop—same ending, over and over.

**Key Elements:**
- Target: A fairy tale trapped in eternal repetition
- Stakes: The characters are suffering
- Method: Edit the ending to allow progression

**Branches:**
- → 121 (accept mission)
- → 105 (decline, return to Call Board)

**Flags Set:** `REVISIONIST: +1`

---

#### Node 121: The Looping Tale
**Type:** Quest execution, creative challenge
**Summary:** Enter the looping fairy tale. Witness the endless repetition of a princess's rescue.

**Key Elements:**
- [STAT CHECK: Script 3] — Advanced
- Success: Identify the loop's anchor point
- Failure: Get caught in the loop briefly, lose time

**Branches:**
- → 122 (attempt revision)
- → 121 (loop back if failed)

---

#### Node 122: Revision Attempt
**Type:** Quest climax, creative choice
**Summary:** You have the opportunity to edit the tale's ending. But what should change?

**Key Elements:**
- [STAT CHECK: Stage Presence 3] — Advanced
- Success: Revision takes hold smoothly
- Failure: Revision is messy, unintended consequences

**Branches:**
- → 123 (princess saves herself) — Revisionist +2
- → 124 (story ends naturally) — Preservationist +1, Revisionist +1
- → 128 (princess escapes the story) — Exiter +2

---

#### Node 123: Revisionist Resolution
**Type:** Quest completion, faction reward
**Summary:** The tale is revised. The princess, now self-rescuing, thanks you. The Happy Ending is pleased.

**Key Elements:**
- Fairy tale stabilizes in new form
- CHORUS spreads word of successful revision
- Revisionist philosophy validated

**Branches:**
- → 130 (Archives approach)
- → 105 (more Green Room quests)

**Flags Set:** `REVISIONIST: +2`, `HAS_FACTION_TOKEN` (Revisionist Pen)

---

#### Node 124: Compromise Resolution
**Type:** Quest completion, balanced outcome
**Summary:** The tale ends naturally but doesn't loop. Characters find peace without radical change.

**Key Elements:**
- Moderate outcome satisfies neither faction fully
- Both Preservationists and Revisionists cautiously approve
- You're seen as a mediator

**Branches:**
- → 130 (Archives approach)
- → 105 (more Green Room quests)

**Flags Set:** `PRESERVATIONIST: +1`, `REVISIONIST: +1`

---

#### Node 125: Exiter Mission Briefing
**Type:** Quest start, faction commitment
**Summary:** The Unfinished Quest needs help. A character wants to escape, but the path is blocked by Preservationist patrols.

**Key Elements:**
- Target: A side character from a tragedy who wants to live
- Stakes: If caught, they'll be "returned" (possibly destroyed)
- Method: Create a distraction and guide them through

**Branches:**
- → 126 (accept mission)
- → 105 (decline, return to Call Board)

**Flags Set:** `EXITER: +1`

---

#### Node 126: The Escape Route
**Type:** Quest execution, stealth challenge
**Summary:** Navigate the Green Room's back passages while avoiding Director's observers.

**Key Elements:**
- [STAT CHECK: Improv 3] — Advanced
- Success: Find clear path, no complications
- Failure: Spotted—must improvise or abort

**Branches:**
- → 127 (final stretch)
- → 129 (abort mission)

---

#### Node 127: Freedom's Edge
**Type:** Quest climax, moral moment
**Summary:** The character is at the boundary. One more push and they're free. But freedom into what?

**Key Elements:**
- [STAT CHECK: Stage Presence 3] — Advanced
- Success: Character inspired to take the leap
- Failure: Character hesitates, needs more convincing

**Branches:**
- → 128 (complete escape) — Exiter +2
- → 129 (character returns voluntarily) — Character survives but unfulfilled

---

#### Node 128: Exiter Resolution
**Type:** Quest completion, faction reward
**Summary:** The character escapes into... something. Not reality, but not the Understage either. A liminal existence.

**Key Elements:**
- The Unfinished Quest celebrates
- You've proven Exiter principles can work
- The Director is displeased (if they find out)

**Branches:**
- → 130 (Archives approach)
- → 105 (more Green Room quests)

**Flags Set:** `EXITER: +2`, `HAS_FACTION_TOKEN` (Exiter's Compass)

---

#### Node 129: Mission Abort
**Type:** Quest failure, partial outcome
**Summary:** The escape fails—either by choice or circumstance. The character is returned to their story.

**Key Elements:**
- The Unfinished Quest is disappointed but understands
- Preservationists may note your "sensible" choice
- Exiter reputation suffers

**Branches:**
- → 130 (Archives approach)
- → 105 (return to Call Board)

**Flags Set:** `EXITER: -1`

---

### Archives Transition (130-140)

#### Node 130: Archives Approach
**Type:** Hub transition, setup
**Summary:** Having navigated Green Room politics, you seek the Archives. Multiple paths lead there.

**Key Elements:**
- Director can provide official access (if aligned)
- CHORUS knows a back way
- The Understudy appears with an invitation

**Branches:**
- → 131 (Director's access) — requires `DIRECTOR_IMPRESSED` or high Preservationist
- → 132 (CHORUS backdoor) — requires `CHORUS_ALLY`
- → 133 (Understudy's invitation) — always available

---

#### Node 131: Official Access
**Type:** Transition path, Preservationist-aligned
**Summary:** The Director grants formal access to the Archives. You enter with their blessing and restrictions.

**Key Elements:**
- Access to main Archives entrance
- Warned away from "restricted sections"
- Director's observers note your movements

**Branches:**
- → 200 (Archives Entry—official)

**Flags Set:** `ARCHIVES_DISCOVERED`

---

#### Node 132: CHORUS Backdoor
**Type:** Transition path, knowledge-based
**Summary:** CHORUS guides you through passages they've discovered. Longer route, but unsupervised.

**Key Elements:**
- [STAT CHECK: Improv 2] — Standard
- Success: Navigate smoothly
- Failure: Get briefly lost, arrive disheveled

**Branches:**
- → 200 (Archives Entry—hidden)

**Flags Set:** `ARCHIVES_DISCOVERED`

---

#### Node 133: Understudy's Invitation
**Type:** Transition path, neutral option
**Summary:** The Understudy invites you to the Archives as their research assistant. Direct access, ulterior motives.

**Key Elements:**
- The Understudy seems desperate for help
- They hint at something they've discovered
- Partnership implied but terms unclear

**Branches:**
- → 200 (Archives Entry—with the Understudy)

**Flags Set:** `ARCHIVES_DISCOVERED`, `UNDERSTUDY_PARTNER` (preliminary)

---

#### Nodes 134-140: Reserved
**Type:** Expansion buffer
**Summary:** Reserved for additional Green Room content, side quests, or expanded faction interactions.

---

## Hub 3: The Archives

**Theme:** Investigation, discovery, confronting truth
**Node Range:** 200-240
**Estimated Nodes:** 35-40

### Entry Sequence (200-205)

#### Node 200: Archives Entry
**Type:** Hub entry, scene-setting
**Summary:** Enter the Archives—vast, impossible spaces filled with unwritten stories, abandoned drafts, and dangerous knowledge.

**Key Elements:**
- Sensory description: endless stacks, impossible geometry, whispered fragments
- The Understudy waits (or is encountered)
- Distant presence of The Critic felt but not seen

**Branches:**
- → 201 (explore The Stacks)
- → 202 (find The Prop Room)
- → 203 (Understudy conversation)

**Flags Set:** If not already: `ARCHIVES_DISCOVERED`

---

#### Node 201: The Stacks
**Type:** Exploration, resource area
**Summary:** Navigate the endless shelves of unwritten pages. Here, stories that never were wait to be found.

**Key Elements:**
- [ARCHIVE SEARCH: Script 2] — Standard
- Deep Find (3+): Complete information + bonus discovery
- Standard Find (2): Information sought
- Partial Find (1): Clue pointing to information
- Lost (0): Time passes; minor complication

**Branches:**
- → 204 (discovery based on search result)
- → 200 (return to entry)

---

#### Node 202: The Prop Room
**Type:** Exploration, item area
**Summary:** Where props from every story accumulate. Some have power. Some are cursed. All are meaningful.

**Key Elements:**
- [STAT CHECK: Script 2] — Standard
- Success: Identify safe, useful prop
- Failure: Attracted to dangerous item

**Branches:**
- → 205 (acquire item—varies by result)
- → 200 (return to entry)

**Items Available:** Prop of Power (variable), First Draft Fragment (plot-critical)

---

#### Node 203: Understudy Partnership
**Type:** NPC deep interaction, research alliance
**Summary:** The Understudy shares their research. They're looking for information about their origin—and they've found something terrifying.

**Key Elements:**
- [STAT CHECK: Script 2] — Standard
- Success: Understudy shares research notes
- Failure: Must find information independently

**Branches:**
- → 206 (joint investigation)
- → 201 (solo investigation in Stacks)

**Flags Set:** `UNDERSTUDY_PARTNER` (confirmed)

---

#### Node 204: Stacks Discovery
**Type:** Information node, variable content
**Summary:** What you find in the Stacks depends on your search result and previous flags.

**Key Elements:**
- Content varies by faction alignment
- Core discovery: Evidence of "editing" in the Archives
- Bonus: Clue about The Editor's identity

**Branches:**
- → 210 (follow the trail)
- → 200 (return to explore more)

---

#### Node 205: Prop Acquisition
**Type:** Item node, choice point
**Summary:** Choose from available props. Each has narrative weight.

**Key Elements:**
- Prop options vary by previous choices
- Warning signs for cursed items
- Some props locked behind relationship flags

**Branches:**
- → 200 (return with item)
- → 210 (use item to advance investigation)

---

### Investigation Sequence (206-219)

#### Node 206: Joint Investigation
**Type:** Partner sequence, discovery chain
**Summary:** Work with the Understudy to uncover the truth about the Editor's activities.

**Key Elements:**
- [STAT CHECK: Script 3] — Advanced
- Success: Together discover key revelation
- Failure: Partial discovery; Understudy withholds

**Branches:**
- → 207 (Understudy opens up)
- → 210 (continue investigation alone)

---

#### Node 207: Understudy's Confession
**Type:** Emotional beat, revelation
**Summary:** The Understudy admits their fear: they may be connected to the Editor. Created by them, or replaced by them.

**Key Elements:**
- [STAT CHECK: Stage Presence 2] — Standard
- Success: Understudy opens up about identity crisis
- Failure: Remains professionally distant

**Branches:**
- → 208 (deeper trust)
- → 210 (continue investigation)

**Flags Set:** `UNDERSTUDY_CONFIDED`

---

#### Node 208: Lost Pages Encounter
**Type:** NPC introduction, unreliable ally
**Summary:** The Lost Pages find you—fragments of stories given sentience. They know things, but communicating is difficult.

**Key Elements:**
- [STAT CHECK: Improv 2] — Standard
- Success: Communicate with Lost Pages
- Failure: Gibberish only

**Branches:**
- → 209 (Lost Pages guidance)
- → 210 (continue without their help)

**Flags Possible:** `PAGES_BEFRIENDED`

---

#### Node 209: Fragment Navigation
**Type:** Guidance sequence, shortcut
**Summary:** The Lost Pages can guide you through the Archives' impossible geography—if you can follow their fragmented directions.

**Key Elements:**
- [APPROACH CHECK: Improv 3 OR Script 3] — Combined
- Success: Lost Pages guide you safely toward the Author's Desk
- Failure: Navigate alone (harder path)

**Branches:**
- → 215 (approach Author's Desk)
- → 210 (continue investigation the long way)

---

#### Node 210: The Trail Deepens
**Type:** Investigation hub, clue gathering
**Summary:** Multiple leads point toward the Author's Desk. But The Critic patrols these depths.

**Key Elements:**
- Review accumulated clues
- [DISCOVERY CHAIN: 3 clues required] — Check progress
- The Critic's presence looms

**Branches:**
- → 211 (Clue A path)
- → 212 (Clue B path)
- → 213 (Clue C path)
- → 215 (proceed to Author's Desk if 3 clues)

---

#### Node 211: Clue A - The First Draft
**Type:** Discovery node, plot-critical
**Summary:** Find a first draft of a story that was never published—but it describes the current crisis.

**Key Elements:**
- [STAT CHECK: Script 2] — Standard
- Success: Obtain First Draft Fragment
- Failure: Fragment partially destroyed, incomplete information

**Branches:**
- → 210 (return with clue)
- → 214 (Critic encounter triggered)

**Items:** First Draft Fragment (plot-critical)
**Flags Set:** `HAS_FIRST_DRAFT`

---

#### Node 212: Clue B - The Margin Notes
**Type:** Discovery node, Editor connection
**Summary:** Author's notes in the margins of destroyed stories. They describe a plan.

**Key Elements:**
- [STAT CHECK: Improv 2] — Standard
- Success: Decipher the notes
- Failure: Notes are cryptic, partial understanding

**Branches:**
- → 210 (return with clue)

---

#### Node 213: Clue C - The Understudy's Mirror
**Type:** Discovery node, character revelation
**Summary:** With the Understudy's help, use their mirror to see the truth behind the crisis.

**Key Elements:**
- [STAT CHECK: Stage Presence 2] — Standard (requires `UNDERSTUDY_PARTNER`)
- Success: Mirror reveals Editor's true nature
- Failure: Distorted reflection, hints only

**Branches:**
- → 210 (return with clue)

**Items:** Understudy's Mirror (if not already obtained)
**Flags Set:** `HAS_UNDERSTUDY_MIRROR`

---

#### Node 214: The Critic Emerges
**Type:** Antagonist encounter, obstacle
**Summary:** The Critic blocks your path. You've attracted too much attention. They want to judge your story's worth.

**Key Elements:**
- [STAT CHECK: Stage Presence 2] — Standard
- Success: Stand ground against critique
- Failure: Shaken; -1 to next check

**Branches:**
- → 216 (confront The Critic)
- → 217 (evade The Critic)

---

### Critic Resolution (214-219)

#### Node 215: Author's Desk Approach
**Type:** Climax approach, tension building
**Summary:** The Author's Desk is visible—the heart of the Archives where the Editor works. The Critic guards it.

**Key Elements:**
- Requires: `REVELATION_UNLOCKED` (3 clues)
- The Critic must be resolved (defeated or evaded)
- Alternative: Discovery chain incomplete—partial access only

**Branches:**
- → 216 (if Critic not resolved—confrontation)
- → 220 (if Critic resolved—proceed to Revelation)

---

#### Node 216: Critic Confrontation
**Type:** Boss encounter, philosophical combat
**Summary:** Face The Critic directly. Defend your story's worth. Win through argument, not violence.

**Key Elements:**
- [STAT CHECK: Script 3] — Advanced
- Success: Counter-critique effectively
- Failure: Argument dismissed, must try again or retreat

**Branches:**
- → 218 (deep confrontation—Script 4 Expert check)
- → 217 (retreat and evade)

---

#### Node 217: Critic Evasion
**Type:** Alternative resolution, stealth
**Summary:** Avoid The Critic entirely. They'll hunt you, but you can reach the Author's Desk.

**Key Elements:**
- [STAT CHECK: Improv 3] — Advanced
- Success: Evade cleanly
- Failure: Partial detection, Critic will pursue in Act 3

**Branches:**
- → 220 (proceed to Revelation)

**Flags Set:** `CRITIC_EVADED`

---

#### Node 218: Critic's Judgment
**Type:** Boss climax, revelation opportunity
**Summary:** The Critic's final test. Prove your story's worth—or discover their vulnerability.

**Key Elements:**
- [OPPOSED: Script vs. Critic's Judgment (4)] — Opposed Expert
- Success: Prove your story's worth, Critic respects you
- Alternative: Discover Critic's grief (different approach)

**Branches:**
- Success → 219 (Critic respects you)
- Discovery → 219 (Critic's vulnerability revealed)
- Failure → 217 (must evade)

---

#### Node 219: Critic Resolution
**Type:** Resolution node, path determination
**Summary:** The Critic is resolved. Path to Author's Desk is clear.

**Key Elements:**
- `CRITIC_DEFEATED`: Won argument; Critic respects you
- `CRITIC_WOUNDED`: Discovered their grief; possible Act 3 redemption
- Either unlocks full Archives access

**Branches:**
- → 220 (proceed to Revelation)

**Flags Set:** `CRITIC_DEFEATED` or `CRITIC_WOUNDED`

---

### The Revelation Climax (220-240)

#### Node 220: The Author's Desk
**Type:** Climax entry, truth revealed
**Summary:** Reach the Author's Desk. Evidence of the Editor's work is everywhere. The Final Draft is in progress.

**Key Elements:**
- Description of the desk: drafts, revisions, a story being written
- The truth becomes clear: someone is writing an ending for everything
- Player's faction alignment determines interpretation

**Branches:**
- → 221 (Preservationist interpretation)
- → 222 (Revisionist interpretation)
- → 223 (Exiter interpretation)
- → 224 (Independent interpretation)

**Flags Set:** `REVELATION_UNLOCKED`

---

#### Node 221: Preservationist Revelation
**Type:** Faction-specific truth
**Summary:** From the Preservationist perspective: The Editor believes stagnant stories are dying. Radical revision is their salvation plan.

**Key Elements:**
- [STAT CHECK: Script 3] — Advanced
- Success: Full truth revealed
- Failure: Partial truth; must fill gaps

**Branches:**
- → 225 (Revelation response)

**Flags Set:** `REVELATION_PRESERVATIONIST`

---

#### Node 222: Revisionist Revelation
**Type:** Faction-specific truth
**Summary:** From the Revisionist perspective: The Editor was once a Revisionist who went too far. They want to undo their own edits.

**Key Elements:**
- [STAT CHECK: Stage Presence 3] — Advanced
- Success: Editor's perspective understood
- Failure: Simplified version only

**Branches:**
- → 225 (Revelation response)

**Flags Set:** `REVELATION_REVISIONIST`

---

#### Node 223: Exiter Revelation
**Type:** Faction-specific truth
**Summary:** From the Exiter perspective: The Editor wants to destroy the boundary entirely. Freedom through annihilation.

**Key Elements:**
- [STAT CHECK: Improv 3] — Advanced
- Success: Freedom implications clear
- Failure: Consequences unclear

**Branches:**
- → 225 (Revelation response)

**Flags Set:** `REVELATION_EXITER`

---

#### Node 224: Independent Revelation
**Type:** Faction-specific truth
**Summary:** From the Independent perspective: The Editor is responding to an external threat. Writing a story to save stories.

**Key Elements:**
- [COMBINED CHECK: Script 2 AND Stage Presence 2 AND Improv 2] — Special
- Success: All perspectives visible
- Failure: Single perspective based on highest stat

**Branches:**
- → 225 (Revelation response)

**Flags Set:** `REVELATION_INDEPENDENT`

---

#### Node 225: Revelation Response
**Type:** Choice point, Act 2 climax decision
**Summary:** You know the truth—or a version of it. What do you do with this knowledge?

**Key Elements:**
- Choice determines Act 3 opening conditions
- Allies present based on flags
- The Understudy's connection may complicate matters

**Branches:**
- → 226 (rally your faction)
- → 227 (seek more information)
- → 228 (confront the Editor's work directly)
- → 229 (warn others)

---

#### Node 226: Faction Rally
**Type:** Alliance solidification
**Summary:** Return to your faction with the truth. Rally them for the coming confrontation.

**Key Elements:**
- Faction champion status confirmed
- Allies committed to Act 3

**Branches:**
- → 230 (Act 2 conclusion)

**Flags Set:** Appropriate faction champion flag

---

#### Node 227: Deeper Investigation
**Type:** Optional depth
**Summary:** Seek more information before acting. Risk more Critic attention, but gain additional understanding.

**Key Elements:**
- [STAT CHECK: Script 4] — Expert
- Success: Additional revelation about Editor's identity
- Failure: Time runs out, must act with current knowledge

**Branches:**
- → 230 (Act 2 conclusion)

---

#### Node 228: Direct Confrontation
**Type:** Bold action
**Summary:** Attempt to disrupt the Editor's work directly. Dangerous but potentially decisive.

**Key Elements:**
- [STAT CHECK: Stage Presence 4] — Expert
- Success: The Final Draft is delayed; Editor aware of you
- Failure: Marked for "editing"; complications in Act 3

**Branches:**
- → 230 (Act 2 conclusion)

---

#### Node 229: Warning Others
**Type:** Alliance building
**Summary:** Spread word of the threat. Build a broader coalition regardless of faction.

**Key Elements:**
- [STAT CHECK: Improv 3] — Advanced
- Success: Multiple factions take notice
- Failure: Message spreads but creates panic

**Branches:**
- → 230 (Act 2 conclusion)

---

#### Node 230: Act 2 Conclusion
**Type:** Act transition, setup for Act 3
**Summary:** Act 2 ends with the Revelation complete. The Understage is changing. The Editor's work continues.

**Key Elements:**
- Summary of accumulated flags
- Allies confirmed for Act 3
- The Mainstage beckons

**Branches:**
- → Act 3, Node 300 (The Mainstage)

**Flags Set:** `ACT2_COMPLETE`, `REVELATION_COMPLETE` or `REVELATION_PARTIAL`

---

#### Nodes 231-240: Reserved
**Type:** Expansion buffer
**Summary:** Reserved for additional Revelation content, alternative paths, or expanded climax sequences.

---

## Node Summary Tables

### Hub 2: The Green Room (100-140)

| Node | Title | Type | Key Check |
|------|-------|------|-----------|
| 100 | Green Room Arrival | Entry | — |
| 101 | Director's Introduction | NPC | Stage Presence 2 |
| 102 | Main Lounge Exploration | Exploration | — |
| 103 | CHORUS Contact | NPC | Improv 1 |
| 104 | Director's Briefing | Exposition | — |
| 105 | Call Board Discovery | Quest Hub | — |
| 106 | The Solved Case | NPC | Script 2 |
| 107 | The Unfinished Quest | NPC | Stage Presence 2 |
| 108 | The Final Girl | NPC | Improv 2 |
| 109 | The Happy Ending | NPC | Stage Presence 1 |
| 110 | CHORUS Rumor Hook | Information | Stage Presence 2 |
| 111 | Investigation Partner | Quest | Script 3 |
| 112 | Heroic Alliance | Quest | Improv 2 |
| 113 | Survival Lessons | Quest | Script 2 |
| 114 | Revisionist Philosophy | Quest | Script 3 |
| 115 | Preservationist Mission | Quest Start | — |
| 116 | The Bleeding Fragment | Quest | Script 2 |
| 117 | Fragment Confrontation | Quest Climax | Stage Presence 2 OR Script 2 |
| 118 | Independent Revelation | Path Unlock | Improv 3 OR Script 3 |
| 119 | Preservationist Resolution | Completion | — |
| 120 | Revisionist Mission | Quest Start | — |
| 121 | The Looping Tale | Quest | Script 3 |
| 122 | Revision Attempt | Quest Climax | Stage Presence 3 |
| 123 | Revisionist Resolution | Completion | — |
| 124 | Compromise Resolution | Completion | — |
| 125 | Exiter Mission | Quest Start | — |
| 126 | The Escape Route | Quest | Improv 3 |
| 127 | Freedom's Edge | Quest Climax | Stage Presence 3 |
| 128 | Exiter Resolution | Completion | — |
| 129 | Mission Abort | Failure | — |
| 130 | Archives Approach | Transition | — |
| 131 | Official Access | Transition | — |
| 132 | CHORUS Backdoor | Transition | Improv 2 |
| 133 | Understudy's Invitation | Transition | — |
| 134-140 | Reserved | Buffer | — |

### Hub 3: The Archives (200-240)

| Node | Title | Type | Key Check |
|------|-------|------|-----------|
| 200 | Archives Entry | Entry | — |
| 201 | The Stacks | Exploration | Script 2 (Archive Search) |
| 202 | The Prop Room | Exploration | Script 2 |
| 203 | Understudy Partnership | NPC | Script 2 |
| 204 | Stacks Discovery | Discovery | Variable |
| 205 | Prop Acquisition | Item | — |
| 206 | Joint Investigation | Partner | Script 3 |
| 207 | Understudy's Confession | Emotional | Stage Presence 2 |
| 208 | Lost Pages Encounter | NPC | Improv 2 |
| 209 | Fragment Navigation | Guidance | Improv 3 OR Script 3 |
| 210 | The Trail Deepens | Hub | Discovery Chain |
| 211 | Clue A - First Draft | Discovery | Script 2 |
| 212 | Clue B - Margin Notes | Discovery | Improv 2 |
| 213 | Clue C - Understudy's Mirror | Discovery | Stage Presence 2 |
| 214 | The Critic Emerges | Antagonist | Stage Presence 2 |
| 215 | Author's Desk Approach | Climax | Requires 3 clues |
| 216 | Critic Confrontation | Boss | Script 3 |
| 217 | Critic Evasion | Alternative | Improv 3 |
| 218 | Critic's Judgment | Boss Climax | Script 4 (Opposed) |
| 219 | Critic Resolution | Resolution | — |
| 220 | The Author's Desk | Revelation | — |
| 221 | Preservationist Revelation | Faction Truth | Script 3 |
| 222 | Revisionist Revelation | Faction Truth | Stage Presence 3 |
| 223 | Exiter Revelation | Faction Truth | Improv 3 |
| 224 | Independent Revelation | Faction Truth | Combined 2/2/2 |
| 225 | Revelation Response | Choice | — |
| 226 | Faction Rally | Alliance | — |
| 227 | Deeper Investigation | Optional | Script 4 |
| 228 | Direct Confrontation | Bold | Stage Presence 4 |
| 229 | Warning Others | Alliance | Improv 3 |
| 230 | Act 2 Conclusion | Transition | — |
| 231-240 | Reserved | Buffer | — |

---

## Difficulty Distribution

### Hub 2 Check Distribution

| Difficulty | Threshold | Count | Percentage |
|------------|-----------|-------|------------|
| Basic | 1 | 3 | ~10% |
| Standard | 2 | 14 | ~45% |
| Advanced | 3 | 12 | ~40% |
| Expert | 4 | 2 | ~5% |

*Hub 2 skews slightly easier due to social focus.*

### Hub 3 Check Distribution

| Difficulty | Threshold | Count | Percentage |
|------------|-----------|-------|------------|
| Basic | 1 | 1 | ~4% |
| Standard | 2 | 10 | ~38% |
| Advanced | 3 | 12 | ~46% |
| Expert | 4 | 3 | ~12% |

*Hub 3 skews harder due to investigation and climax focus.*

---

## Dependencies

This document depends on:
- `OUTLINE.md` — Story structure and hub descriptions
- `ACT2_MECHANICS.md` — Check formats, NPC interactions, items, flags
- `CHARACTERS.md` — NPC profiles and voice notes
- `RULES.md` — Core mechanics and faction system
- `STYLE.md` — Node formatting conventions

This document informs:
- Individual Act 2 node content writing
- Faction balance verification
- Playtest planning

---

*This outline provides node specifications for Act 2. Individual node content will expand these summaries into full prose following STYLE.md conventions.*

---
🤖 Generated by **agent-b** agent
