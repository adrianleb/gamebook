## Node 205: Prop Acquisition

*The Archives — The Prop Room*

The Prop Room waits for your choice.

Around you, the objects of a thousand stories gleam and shadow. Every prop carries weight—not physical weight, but the narrative weight of what it meant, what it did, what it could do again. Choosing wisely is as important as choosing at all.

The Understudy stands at your shoulder, their earlier assessment fresh in both your minds.

---

### If you have `PROP_SAFE_CHOICE`:

Your careful reading of the props paid off. You know which items are truly useful and which are traps dressed in theatrical shine.

**The Understudy:** "Good eye. You can tell the difference between set dressing and the real thing."

You examine your options with confidence:

**The First Draft Fragment** — A piece of original manuscript, its pages carrying the weight of first intention. In a place built on revision, original text has power. This fragment could reveal truths that later versions tried to hide.
*Artifact, Plot-Critical. Counts toward Revelation clue collection.*

**A Ring of Keys** — Not all of them, but one in particular: a key made of compressed shadow that feels cold in your hand. It opens doors that exist only when you need them.
*Tool. One-time use: create passage through a narrative barrier.*

**The Understudy's Mirror** — The Understudy notices you eyeing this and shakes their head. "That one's mine. I've been looking for it—it's a piece of my original's story." They pick it up reverently. "But I'll share it. It shows people as they truly are. Or as they were. Or as they're meant to be."
*Artifact. Reveals character truth. Shared with Understudy.*

**Your Choice:**
You may take ONE of the following:
1. Take the First Draft Fragment (plot-critical, advances Revelation) → Sets `HAS_FIRST_DRAFT`
2. Take the Shadow Key (utility, creates new paths) → Sets `HAS_SHADOW_KEY`
3. Let the Understudy keep the Mirror and take nothing for yourself → Sets `UNDERSTUDY_HAS_MIRROR`, increases trust

---

### If you have `PROP_REDIRECTED`:

The Understudy's intervention saved you from a cursed prop, but it also limited your options. The safest items aren't the most powerful.

**The Understudy:** "Sorry about grabbing you like that. But that sword... I've read about it. The wielder always wins the fight, but they never stop fighting. Eternal combat until they're nothing but the echo of a war cry."

They guide you toward the safer section of the Prop Room. The options here are less dramatic but genuinely useful:

**A Bundle of Blank Pages** — Pages that haven't been written yet. In the Archives, where everything is text, blank pages are potential. They could become notes, maps, or messages to people who haven't been met.
*Script. Consumable: write three short messages that become true when read.*

**A Candle of Continuity** — A prop from a story that never ended. Its flame shows the connections between things: how one scene leads to another, how choices connect to consequences.
*Tool. Reveals narrative connections in a scene.*

**Wrapped Bandages** — They look mundane, but they're from a story about a healer who never failed. Wearing them won't make you invincible, but it might help you recover from a narrative setback.
*Healing. One-time use: recover from a failed check without consequences.*

**Your Choice:**
You may take ONE of the following:
1. Take the Blank Pages (utility, communication) → Sets `HAS_BLANK_PAGES`
2. Take the Candle of Continuity (investigation aid) → Sets `HAS_CONTINUITY_CANDLE`
3. Take the Healing Bandages (safety net) → Sets `HAS_HEALER_BANDAGES`

---

After making your choice, the Understudy nods in approval.

**The Understudy:** "That's a good choice. It won't solve everything, but nothing here would. These are props, not solutions. They help you play your role—they don't change what the role is."

They gesture toward the Prop Room's exit.

**The Understudy:** "We should keep moving. The Archives are vast, and we've only scratched the surface. Whatever's happening here—the disturbances, the editing—we're going to need more than props to understand it."

---

**Choices:**

1. Return to the Archives entry hall → Node 200
2. *[If `AUTHOR_DESK_KNOWN` or `AUTHOR_DESK_HINTED`]* Follow the trail toward the Author's Desk → Node 210

---

**Notes:**
- The safe choice path offers stronger narrative items; the redirected path offers practical utilities.
- Item choices create different approaches to later Archives challenges.
- The Understudy's Mirror is only available if the player made the safe choice AND chose option 3, demonstrating narrative generosity.

---
