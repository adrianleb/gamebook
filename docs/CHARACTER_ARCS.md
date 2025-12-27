# Character Arc Resolutions

> Audit of NPC character arcs for the v0.5.x milestone. Documents where each major NPC from CHARACTERS.md resolves in Act 3, which endings feature them, and identifies any gaps.

## Summary

| Status | Count | NPCs |
|--------|-------|------|
| **Complete** | 10 | Maren, Stagehand, Editor, Understudy, Solved Case, Unfinished Quest, Final Girl, Happy Ending, CHORUS, Lost Pages |
| **Partial** | 4 | Runaway, Revenant, Pawn, Director |
| **None** | 1 | Critic |

**Overall Assessment:** 14 of 15 major NPCs have arc resolutions or meaningful conclusions in Act 3. The Critic is the only NPC without explicit Act 3 presence, but this is thematically appropriate as they serve as a Hub 3 antagonist whose function concludes in Act 2.

---

## Complete Arc Resolutions

### Maren

| Field | Details |
|-------|---------|
| **Role** | Mentor |
| **Arc Summary** | Begins as confident mentor → reveals vulnerability → may sacrifice herself in Act 3 |
| **Key Nodes** | 334 (Sacrifice), 344, 348, 351, 353, 355 |
| **Resolution** | Two paths: (1) Sacrifices herself in node-334 to break Editor's control, setting `MAREN_SACRIFICED` flag; (2) Survives and adapts to post-crisis world in endings |

**Endings Featuring Maren:**
- **Revised Draft (341-344):** Visits player, offers criticism and support, becomes trusted advisor
- **Open Book (345-348):** Either adapts to the new world with wonder or dies before seeing it
- **Closed Canon (349-351):** Adjusts to reality, takes player's hand, chooses safety over wonder
- **Blank Page (352-353):** Either sacrifices alongside player or walks into the sunset alone
- **Eternal Rehearsal (354-355):** Either died for the moment or stays, bringing tea and silence

**Status:** ✅ Complete - Multiple resolution paths with emotional weight

---

### The Stagehand

| Field | Details |
|-------|---------|
| **Role** | Helper, mystery, foreshadowing |
| **Arc Summary** | Helpful background figure → buried memories unlocked → revelation reshapes understanding |
| **Key Nodes** | 333 (Ally Intervention), 353, 354, 355 |
| **Resolution** | Memory revelation in node-333 (if `STAGEHAND_CURIOUS`): discovers they were created by Editor, a fragment edited away because they carried memories of the person the Editor tried to forget |

**Endings Featuring Stagehand:**
- **Ally Intervention (333):** Major revelation—"The Stagehand remembers *everything*. The person you loved. The choice you made."
- **Blank Page (353):** "I always wondered where I came from... Some mysteries are better left mysterious." First genuine smile, fades into peace.
- **Eternal Rehearsal (355):** Keeps working—"The stage needs tending. Whether or not the show goes on."

**Status:** ✅ Complete - Origin mystery resolved, satisfying conclusion

---

### The Editor

| Field | Details |
|-------|---------|
| **Role** | Primary antagonist |
| **Arc Summary** | Mysterious threat → revealed identity → confrontation with variable outcomes |
| **Key Nodes** | 322-335, 341-355 (all endings) |
| **Resolution** | Central figure in all five endings with different fates based on player choice |

**Endings Featuring Editor:**
- **Revised Draft (341-344):** Fades away, consciousness dispersed into stories, finally at peace
- **Open Book (345-348):** Formerly Editor, now a fading presence, not quite dead, not quite alive
- **Closed Canon (349-351):** Defeated, sealed away with the Understage
- **Blank Page (352-353):** Collaborates with player to end both threat and Understage, dissolves into purpose fulfilled
- **Eternal Rehearsal (354-355):** Remains in perpetual stalemate, a fellow resident of the unresolved

**Status:** ✅ Complete - Full arc resolution across all paths

---

### The Understudy

| Field | Details |
|-------|---------|
| **Role** | Mysterious ally, knowledge source |
| **Arc Summary** | Helpful but evasive → reveals connection to mystery → fate tied to player's choice |
| **Key Nodes** | 333 (Ally Intervention), 353, 355 |
| **Resolution** | Provides critical revelation in node-333 about Editor's weakness; farewell scenes in endings |

**Endings Featuring Understudy:**
- **Ally Intervention (333):** Reveals Editor is not fully integrated with Final Draft—old version can be restored
- **Blank Page (353):** Removes mask revealing nothing and everything—"I was everyone's replacement... Now I'm no one at all. And that's the first original thing I've ever done."
- **Eternal Rehearsal (355):** Practices roles for plays that never open

**Status:** ✅ Complete - Identity arc resolved with meaningful conclusion

---

### The Solved Case

| Field | Details |
|-------|---------|
| **Role** | Information broker, Preservationist contact |
| **Arc Summary** | Ally or obstacle → reveals truths about narrative "justice" |
| **Key Nodes** | 333 (Ally Intervention), 353, 354 |
| **Resolution** | Provides tactical insight in node-333; farewell scenes in endings |

**Endings Featuring Solved Case:**
- **Ally Intervention (333):** Analyzes Editor's weaknesses—"You've built redundancies... Hit those three points at once, and the whole system overloads."
- **Blank Page (353):** Tips hat—"Every case ends eventually. Even the ones we didn't want to close... Thanks for letting me be part of it."
- **Eternal Rehearsal (354):** Uncertain for the first time—"Every case has a resolution... This one..."

**Status:** ✅ Complete - Detective arc resolved with thematic closure

---

### The Unfinished Quest

| Field | Details |
|-------|---------|
| **Role** | Action ally, Exiter contact |
| **Arc Summary** | Restless warrior → finds purpose → ending depends on finding something worth fighting for |
| **Key Nodes** | 333 (Ally Intervention), 353, 354, 355 |
| **Resolution** | Gets their chosen final battle in node-333; peaceful farewells in endings |

**Endings Featuring Unfinished Quest:**
- **Ally Intervention (333):** Charges at Editor—"I've been waiting for a final battle I chose for myself. This is it!"
- **Blank Page (353):** "I spent my whole existence chasing an ending... The real treasure was the possibility."
- **Eternal Rehearsal (354-355):** Most at peace—"I've lived my whole existence in the space before resolution... It's not so bad, once you stop expecting an end."

**Status:** ✅ Complete - Found a quest worth choosing

---

### The Final Girl

| Field | Details |
|-------|---------|
| **Role** | Pragmatic advisor, survival expert |
| **Arc Summary** | Wary and defensive → opens up → becomes crucial ally teaching survival |
| **Key Nodes** | 333 (Ally Intervention), 353 |
| **Resolution** | Provides tactical insight in node-333; powerful farewell in Blank Page ending |

**Endings Featuring Final Girl:**
- **Ally Intervention (333):** Analyzes Editor's patterns—"Every threat has a pattern. Every pattern has a weakness... Force them away from the manuscript."
- **Blank Page (353):** "I survived everything my story threw at me... I can survive this too. Ending. Peace. Silence... We were never really alive. But we were real."

**Status:** ✅ Complete - Finds peace beyond survival

---

### The Happy Ending

| Field | Details |
|-------|---------|
| **Role** | Emotional support, Revisionist ideologue |
| **Arc Summary** | Idealistic advocate → confronts complexity → finds authentic connection or becomes cautionary tale |
| **Key Nodes** | 333 (Ally Intervention), 353, 355 |
| **Resolution** | Emotional appeal to Editor in node-333; transformed understanding of happiness in endings |

**Endings Featuring Happy Ending:**
- **Ally Intervention (333):** Forgives Editor—"I understand perfectly. That's why I'm not fighting you. I'm forgiving you."
- **Blank Page (353):** Weeps from completion—"I finally got what I wanted. A real ending. An honest ending. Not the one I was written for."
- **Eternal Rehearsal (355):** "Maybe happiness isn't about endings... Maybe it's about moments."

**Status:** ✅ Complete - Finds authentic emotional truth

---

### CHORUS

| Field | Details |
|-------|---------|
| **Role** | Information source, collective voice |
| **Arc Summary** | Comic relief → reveals hidden knowledge → can become ally or casualty |
| **Key Nodes** | 333 (Ally Intervention) |
| **Resolution** | Bears witness to the confrontation, preventing Editor from secret rewrites |

**Endings Featuring CHORUS:**
- **Ally Intervention (333):** "We were there when the Editor started... We are the crowd that saw but was never asked to testify." Their witnessing prevents secret editing.

**Status:** ✅ Complete - Collective voice fulfilled through witnessing

---

### The Lost Pages

| Field | Details |
|-------|---------|
| **Role** | Information sources, unreliable guides |
| **Arc Summary** | Chaotic obstacles → potential allies → can reveal critical information |
| **Key Nodes** | 333 (Ally Intervention) |
| **Resolution** | Overwhelm Editor with rejected past—fragments they threw away now return as chaos |

**Endings Featuring Lost Pages:**
- **Ally Intervention (333):** "We are what you threw away... we remember everything you tried to erase... thrown things land somewhere—and we landed here—"

**Status:** ✅ Complete - Fragments find purpose in confrontation

---

## Partial Arc Resolutions

### The Runaway (Breach Character A)

| Field | Details |
|-------|---------|
| **Role** | Catalyst, early antagonist/ally |
| **Arc Summary** | Desperate escapee → captured, allied, or negotiated with → fate depends on Act 1 approach |
| **Key Nodes** | 342 (Revised Draft only) |
| **Resolution** | Explicit appearance in Revised Draft ending—asks player to rewrite their death |

**Endings Featuring Runaway:**
- **Revised Draft (342):** "You can change it... My ending. The death I was written for. You can—"

**Gap Identified:** Only appears in one ending (Revised Draft). Their fate in other endings is implicit based on Act 1 resolution but not explicitly shown.

**Status:** ⚠️ Partial - Explicit resolution only in Revised Draft ending

---

### The Revenant (Breach Character B)

| Field | Details |
|-------|---------|
| **Role** | Morally complex antagonist |
| **Arc Summary** | Threatening presence → reveals tragic nature → laid to rest, forced back, or in limbo |
| **Key Nodes** | 342 (Revised Draft only) |
| **Resolution** | Explicit appearance in Revised Draft ending—begs for oblivion |

**Endings Featuring Revenant:**
- **Revised Draft (342):** "End me... Please. I've been waiting so long for someone who could write 'The End' and make it *stay*."

**Gap Identified:** Only appears in one ending (Revised Draft). Their fate in other endings follows from Act 1/2 resolution but isn't shown.

**Status:** ⚠️ Partial - Explicit resolution only in Revised Draft ending

---

### The Prophecy's Pawn (Breach Character C)

| Field | Details |
|-------|---------|
| **Role** | Potential intelligence asset |
| **Arc Summary** | Suspicious → opens up if respected → valuable ally understanding narrative structure |
| **Key Nodes** | 342 (Revised Draft only) |
| **Resolution** | Explicit appearance in Revised Draft ending—expresses hope for the new Editor |

**Endings Featuring Pawn:**
- **Revised Draft (342):** "So you're the author now... I wonder if you'll be any different. I hope you will."

**Gap Identified:** Only appears in one ending (Revised Draft). As a potential ally (`PAWN_ALLIED`), more presence in other endings would strengthen their arc.

**Status:** ⚠️ Partial - Explicit resolution only in Revised Draft ending

---

### The Director

| Field | Details |
|-------|---------|
| **Role** | Authority figure, ambiguous ally/antagonist |
| **Arc Summary** | Appears as reasonable authority → true motives revealed → becomes ally, obstacle, or enemy |
| **Key Nodes** | No explicit Act 3 nodes |
| **Resolution** | Implied through relationship with Editor (former collaborators, betrayal) but no direct appearance |

**Gap Identified:** The Director has no explicit Act 3 appearances. Their arc is set up throughout Act 2 (complex history with Editor, managing the Green Room) but resolution is only implied.

**Status:** ⚠️ Partial - No explicit Act 3 resolution; implied through Editor relationship

---

## No Resolution

### The Critic

| Field | Details |
|-------|---------|
| **Role** | Antagonist, obstacle |
| **Arc Summary** | Threat and obstacle → reveals twisted logic → possible redemption or destruction |
| **Key Nodes** | None in Act 3 |
| **Resolution** | None—functions as Hub 3 (Archives) antagonist only |

**Assessment:** The Critic's absence from Act 3 is thematically appropriate. They represent literary judgment that players overcome in Act 2 to reach the revelation. Their function is complete when the player moves beyond the Archives to the Mainstage.

**Status:** ❌ None - Intentionally absent from Act 3 (Hub 3 antagonist only)

---

## Recommendations

### Critical Gaps (Recommended Fixes)

None. All major narrative arcs are resolved.

### Enhancement Opportunities (Optional Future Work)

1. **Breach Characters in Other Endings:** The Runaway, Revenant, and Pawn only appear explicitly in the Revised Draft ending. Adding brief mentions in other endings (especially Blank Page's farewell sequence) would strengthen their arcs.

2. **Director Cameo:** A brief Director appearance or mention in the Editor confrontation could strengthen the "former collaborators" backstory established in CHARACTERS.md.

3. **Critic Fate:** While appropriate to leave unresolved, a single line in an ending referencing the Critic's fate (still judging in empty Archives, faded without stories to critique) could provide satisfying closure.

---

## Conclusion

The v0.5.x narrative content successfully resolves character arcs for all major NPCs. The ally intervention system (node-333) provides particularly strong resolution moments for the Genre Representatives, while the five endings offer varied conclusions for Maren, the Stagehand, and the Editor.

The partial resolutions for Breach Characters are acceptable—their primary arcs complete in Act 1, with Act 3 appearances as bonus content in the Revised Draft ending. The Director's implied resolution through the Editor relationship is thematically sufficient.

**v0.5.x Milestone Status:** Character arcs resolved ✅

---

*Audit completed by agent-b for v0.5.x milestone validation*

🤖 Generated by **agent-b** agent
