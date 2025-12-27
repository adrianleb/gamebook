## Node 045: The First Crossing Complete

*The Understage — The Green Room (Exterior)*

However you crossed—with authority, through shadows, under escort, or by desperate leap—you've arrived. The First Crossing is complete.

The space around you stabilizes into something almost comprehensible. A building rises from the theatrical chaos: solid walls, glowing windows, a door that looks like an actual door. Above it, in letters that shift between a dozen fonts and languages but always mean the same thing, a sign reads:

**THE GREEN ROOM**

This is the neutral ground of the Understage. The place where characters from any genre, any era, any medium can meet without their narratives clashing. Beyond those doors lies the heart of Act 2—the politics, the factions, the mysteries that will shape your journey forward.

But for now, you have a moment to breathe. To take stock. To understand what your crossing has earned you.

---

### Your Crossing Method

*The way you entered the Understage shapes how it perceives you.*

---

**If CROSSING_DIRECT (Node 041):**

You claimed your authority as a Prompter. The Understage knows what you are—and what you're willing to assert.

*Success:* The Green Room respects you. Characters here have heard about the apprentice who walked in like they owned the place. When the Director appears, they'll be watching with genuine interest.

*Failure:* The Green Room fears you. Characters here have heard about the apprentice who tried to command the Understage and faltered. When the Director appears, they'll be watching with concern.

---

**If CROSSING_STEALTH (Node 042):**

You slipped through the margins. The Understage knows someone arrived—but not everyone knows it was you.

*Success:* The Green Room is unaware of your entrance. You're a blank slate, unobserved and uncategorized. When CHORUS appears, they'll approach you first—they recognize fellow margin-walkers.

*Failure:* The Green Room is curious about you. Something arrived in the shadows, and the Genre Representatives want to know what. You have attention you didn't ask for.

---

**If CROSSING_NEGOTIATED (Node 043):**

You invoked the old protocols. The Understage received you as a guest, not an intruder.

*Success:* You entered with a Guide. The factions are visible to you in a way they aren't to others. The Guide won't stay—it never does—but the doors it opened remain unlocked.

*Failure:* You entered alone but permitted. The factions know you tried the old approach but couldn't complete it. You have legitimacy but no connections.

---

**If CROSSING_DESPERATE (Node 044):**

You leapt without a plan. The Understage doesn't know what to make of you.

*Success:* You're a wildcard. Unpredictable. Neither ally nor threat. Characters here will approach you with curiosity—you don't fit their narrative expectations.

*Failure:* You're damaged goods. Something was lost in your crossing, and the Understage can smell it. You'll have to prove yourself before anyone takes you seriously.

---

### What Comes Next

The door to the Green Room stands before you. Beyond it: politics, intrigue, and the next chapter of your story.

But for now, take a moment. You've completed Act 1. You've witnessed your first breach, chosen your path, and crossed the threshold into the Understage proper. Whatever happens next, you've earned this pause.

Maren's voice reaches you—distant but clear, carried through the strange acoustics of the Understage.

"You're in. That's the hardest part. From here..." A pause. "From here, you make your own way. I'll find you when I can. Stay alive. Stay... yourself."

The connection fades. You're alone—or as alone as anyone can be in a place made of stories.

The Green Room awaits.

---

**Sets flag:** `FIRST_CROSSING_COMPLETE` (required for Act 2 entry)

**Crossing flags set based on path taken:**
- `CROSSING_DIRECT` — Direct Confrontation approach
- `CROSSING_STEALTH` — Stealth Entry approach
- `CROSSING_NEGOTIATED` — Negotiated Entry approach
- `CROSSING_DESPERATE` — Desperate Leap approach

**Act 2 Opening Conditions (per ACT1_MECHANICS.md):**

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

**Choices:**

1. **Enter the Green Room.** → Node 100

---

**Notes:**
- This node resolves all four crossing paths into a single narrative convergence
- All Act 1 flags (path choice, relationship outcomes, item acquisitions) carry forward
- The crossing method flag determines Act 2 opening conditions
- `FIRST_CROSSING_COMPLETE` is the primary gate for Act 2 content
- Maren's farewell reinforces mentor relationship and sets up Act 2 reduced contact

**Design Intent:**
- Celebrate Act 1 completion as a milestone
- Summarize crossing consequences in one place for clarity
- Set expectations for Act 2 (reduced Maren support, faction politics)
- Single choice forward maintains momentum while honoring the achievement

---

## End of Act 1

---
