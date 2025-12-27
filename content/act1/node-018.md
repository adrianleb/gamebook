## Node 018: Resolution

*The Understage — Dead End Stage*

The chase is over. Whatever led you here—capture, compassion, or exhausted negotiation—you and the Runaway have arrived at something like an understanding.

The candles in the set have steadied. The flats stand still. The dead end stage feels less like a trap now and more like a space for conversation. Perhaps that's what it always was, underneath the theatrical dressing.

The Runaway sits in one of the chairs by the painted fireplace. After a moment's hesitation, you take the other. The configuration is absurd—two people having a civil discussion in a tragedy's death scene, the void of unwritten stories pressing at the edges—but it feels right.

"So," they say. "What happens now?"

If you captured them, they're waiting to hear their sentence. If you didn't, they're waiting to hear your terms. Either way, something important is being decided here.

"You're going to bring me back to the Prompter's Booth," they continue. "I know that. I've known since you followed me through the threshold. But what happens after that is still... unwritten."

They look at the painted fireplace, at the chairs, at all the props of their predetermined death.

"I could be contained. Locked away until someone decides what to do with me. Or I could be *revised*—my ending rewritten into something I don't remember choosing. Or..." They trail off.

"Or?" you prompt.

"Or you could vouch for me. Tell your mentor I'm not a threat. That I just... want to choose my own ending. Whatever that ending turns out to be."

It's a lot to ask. You barely know them. You've been a Prompter's apprentice for less than a day. But they're looking at you with the kind of hope that makes you remember: they're not just a character. They're someone who was written to die, and chose to live.

**[APPROACH CHECK: Stage Presence 2 OR Improv 2]**

**Success:** You meet their eyes. Whatever happens next, you've learned something in this chase: characters can grow beyond their scripts. That has to matter.

"I'll speak to Maren," you say. "I can't promise what she'll decide. But I'll tell her you're not the enemy. You're just someone trying to survive."

The Runaway's expression breaks—relief and gratitude and something like hope flooding their features. For a moment, they look almost young. Almost free.

"Thank you," they whisper. "I don't know if that will save me. But it's the first time anyone's treated me like... like my story wasn't already finished."

They rise, and offer you their hand. Not to flee. Not to fight. Just to shake.

"Whatever happens," they say, "I won't forget this. The character who chose to listen."

**Sets flag:** `MAREN_TRUST_HIGH` (if not already set)
**Relationship:** Runaway is cooperative

→ Go to Node 040 (The First Crossing — Pursuers Entry)

**Failure:** You try to reassure them, but the words come out wrong—too formal, too much like a captor making promises. The moment of connection slips away.

The Runaway's expression closes off. They nod, once, accepting their fate.

"I understand," they say, their voice flattening into something rehearsed. "You have your role. I have mine. I just hoped... for a moment... that stories could change."

They stand, waiting to be led back. They're not fighting anymore—but the spark of hope you glimpsed is gone. They've retreated into the character they were written to be: the tragic victim, accepting death.

You've completed your mission. But something's been lost.

**Relationship:** Runaway is wary but compliant

→ Go to Node 040 (The First Crossing — Pursuers Entry)

---

**Flags Set:**
- Success: `MAREN_TRUST_HIGH` (Maren hears of your handling of the situation)
- Both: `RUNAWAY_STATUS_SET` (marker for path completion)

**Notes:**
- This is a Combined Approach check per ACT1_MECHANICS.md—either Stage Presence 2 OR Improv 2 succeeds
- Success: Runaway trusts player; Maren trust bonus; cooperative relationship for Act 2
- Failure: Mission completed but Runaway relationship is damaged; wary stance in Act 2
- This node closes the Pursuers Path before converging at the First Crossing (Node 40+)
- The choice to use either stat makes this accessible to players who invested in different builds

---
