## Node 204: Stacks Discovery

*The Archives — Among the Shelves*

You emerge from the depths of the Stacks with something in your hands. The search yielded results—the question is how much.

The Understudy waits at the edge of the shelves, their anxiety visible in the way they shift from foot to foot. When they see you approaching, they straighten, hope and fear warring in their expression.

**The Understudy:** "Did you find anything? About the disturbances? About..." They trail off, not quite willing to name their own obsession.

You share what you've discovered.

---

### If you have `DEEP_FIND`:

The manuscript you found is comprehensive. More than comprehensive—it's a record of deliberate revision, and the pattern is unmistakable.

**Your Discovery:** Someone has been editing the Archives themselves. Not just individual stories, but the *structure* of the Understage. The manuscript documents changes: characters removed from existence, plot points overwritten, entire narrative arcs redirected. All of it in red ink. All of it signed with a simple initial: *E*.

The margin note you found makes the stakes clear: *"If they find the Author's Desk, we lose everything."*

The Understudy reads over your shoulder, their face draining of color.

**The Understudy:** "The Editor. I've seen that initial in my own research. Whoever wrote me... whoever copied me from the original... they used the same red ink." They look at you with dawning understanding. "You found evidence of what they're doing. And now we know where they're doing it. The Author's Desk."

The discovery unlocks a clear path forward.

**Flags Set:**
- `HAS_EDITOR_EVIDENCE`
- `AUTHOR_DESK_KNOWN`

**Bonus Discovery:** The loose page you found—the one with the warning—seems to be from a different text entirely. It references something called "the Final Draft" and suggests that the Editor is working toward a specific endpoint. What that endpoint means for the Understage... you'll need to investigate further.

**Flags Set:**
- `FINAL_DRAFT_MENTIONED`

→ Continue to exploration: Return to Node 200 or proceed to Node 210 (The Trail Deepens)

---

### If you have `STANDARD_FIND`:

The manuscript you found is useful. It documents disturbances in the Archives—stories being changed, characters going missing, plot points appearing where none existed before. The changes share a common signature: red ink annotations, corrections that feel more like commands.

**Your Discovery:** Someone is revising the Archives. The manuscript doesn't name them, but it points toward a location: the Author's Desk, deep in the Archives, where the unauthorized editing seems to originate.

**The Understudy:** "The Author's Desk..." They nod slowly. "I've seen references to it. A place where stories can be written directly into existence. Or rewritten." They meet your eyes. "If someone's using that kind of power without oversight, it would explain everything—the disturbances, the Director's concern, the faction tensions."

You have a direction. The specifics remain unclear, but the path is visible.

**Flags Set:**
- `AUTHOR_DESK_KNOWN`

→ Continue to exploration: Return to Node 200 or proceed to Node 210 (The Trail Deepens)

---

### If you have `PARTIAL_FIND`:

The fragments you gathered paint an incomplete picture. Something is wrong in the Archives—that much is clear. Stories are changing without authorization. Characters are disappearing or appearing where they shouldn't. There's a pattern, but you can only see its edges.

**Your Discovery:** References to "the Author's Desk" appear across multiple fragments. The location seems significant—a place of power, of writing, of change. But the details scatter before you can grasp them.

**The Understudy:** "The Author's Desk is real, then." They look troubled. "I'd hoped it was just a legend. A story characters tell about where stories come from." They shake their head. "If it's real, and if someone's using it... we need more information."

You have a direction, but not a clear path. More searching is required.

**Flags Set:**
- `AUTHOR_DESK_HINTED`

→ Continue to exploration: Return to Node 200

---

### Variable Content by Faction Alignment:

Depending on your faction alignment from the Green Room, additional context colors your discovery:

**If `PRESERVATIONIST >= 3`:** You recognize the pattern of revision as a violation. The Director's warnings make more sense now—unauthorized editing threatens the stability of every story in the Understage. The Editor isn't just breaking rules; they're undermining the structure that keeps fiction and reality separate.

**If `REVISIONIST >= 3`:** You see something the Preservationists would miss: whoever is doing this has skill. The revisions aren't random destruction—they're deliberate, purposeful changes. The Editor, whoever they are, believes they're *improving* things. Whether that's true... you're not sure yet.

**If `EXITER >= 3`:** The fragment you found mentions characters being "freed" from their narratives. For the Exiters, that might be salvation. But the tone of the document suggests the method is dangerous—freedom through destruction rather than choice. The Editor's approach might share Exiter goals without Exiter ethics.

**If all factions low (Independent):** You see the situation without faction bias. Someone is changing things. The changes might be beneficial or destructive—probably both, depending on perspective. The truth, as always, requires more investigation.

---

**Choices:**

1. Return to the Archives entry hall to explore other areas → Node 200
2. Follow the trail deeper into the Archives → Node 210

---
